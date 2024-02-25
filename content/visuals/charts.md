---
title: "Charts"
date: 2023-05-21
description: "Charts of Doll Demographics"
summary: "Charts of Doll Demographics"
showDate: false
layout: "photo-gallery"

showReadingTime: false
groupByYear: false
showAuthor: false
showWordCount: false
showDate: false
showPagination: false
---

As a data person, I enjoy creating charts and graphs to showcase data and story telling. Here are some of views of my doll collections that I thought would be fun to share.

## Doll Company Demographics
<!-- prettier-ignore-start -->
{{< chart >}}
type: 'bar',
data: {
  labels: [ 'ATSDoll Studio',
            'Black Cherry Dolls',
            'DollShe',
            'Dollstown',
            'Draugar Dolls',
            'Fan/FF Studio',
            'Fifth Motif',
            'Impldoll',
            'Iplehouse',
            'LLT',
            'Meeks Doll',
            'Phoenix Dolls',
            'Pygmalion Dolls',
            'Rugged Realism',
            'Supia Dolls',
        ],
  datasets: [{
    label: 'Heads',
    data: [  1, <!-- ATSDoll Studio --> 
             2, <!-- Black Cherry Dolls --> 
             0, <!-- DollShe --> 
             0, <!-- Dollstown --> 
             2, <!-- Draugar Dolls --> 
             1, <!-- Fan/FF Studio --> 
             1, <!-- Fifth Motif --> 
             1, <!-- Impldoll --> 
             2, <!-- Iplehouse --> 
             1, <!-- LLT --> 
             1, <!-- Meeks Dolls --> 
             1, <!-- Phoenix Dolls --> 
             1, <!-- Pygmalion Dolls --> 
             6, <!-- Rugged Realism --> 
             0, <!-- Supia Dolls --> 
        ],
    backgroundColor: 'rgba(153, 102, 255, 0.2)',
    borderColor: 'rgba(153, 102, 255)',
    borderWidth: 1
  },
  {
    label: 'Bodies',
    data: [ 1, <!-- ATSDoll Studio --> 
            0, <!-- Black Cherry Dolls --> 
            1, <!-- DollShe --> 
            3, <!-- Dollstown --> 
            1, <!-- Draugar Dolls --> 
            1, <!-- Fan/FF Studio --> 
            1, <!-- Fifth Motif --> 
            2, <!-- Impldoll --> 
            1, <!-- Iplehouse --> 
            1, <!-- LLT --> 
            1, <!-- Meeks Dolls --> 
            0, <!-- Phoenix Dolls --> 
            0, <!-- Pygmalion Dolls --> 
            4, <!-- Rugged Realism --> 
            1, <!-- Supia Dolls --> 
        ],
    backgroundColor: 'rgba(54, 162, 235, 0.2)',
    borderColor: 'rgba(54, 162, 235)',
    borderWidth: 1
  },

  ]
},
options: {
    maintainAspectRatio: false,
    indexAxis: 'y',
    scales: {
      x: {
        stacked: true,
        ticks: {
            maxTicksLimit: 20,
            autoSkip: false,
            beginAtZero: true
        }
      },
      y: {
        stacked: true,
        ticks: {
            maxTicksLimit: 20,
            autoSkip: false,
            beginAtZero: true
        }
      }
    },
    plugins: {
            legend: {
                labels: {
                    // This more specific font property overrides the global property
                    font: {
                        weight: 'bold'
                    }
                }
            }
        }
  }
{{< /chart >}}
<!-- prettier-ignore-end -->

## Cumulative Acquistion By Year (Heads & Bodies)

<!-- prettier-ignore-start -->
{{< chart progressiveLine="true" >}}
type: 'line',
data: {
  labels: ['January',
            'February',
            'March',
            'April',
            'May',
            'June',
            'July',
            'August',
            'September',
            'October',
            'November',
            'December'],
  datasets: [{
            label: '2019',
            data: [,,,,,,,,,1,1,2],
            fill: false,
            stepped: 'middle',
        },
        {
            label: '2020',
            data: [2,2,2,2,3,3,3,3,4,4,5,5],
            fill: false,
            stepped: 'middle',
        },
        {
            label: '2021',
            data: [7,9,9,9,10,11,13,13,15,15,15,16],
            fill: false,
            stepped: 'middle',
          },
        {
            label: '2022',
            data: [17,17,17,19,20,20,20,24,24,24,24,24],
            fill: false,
            stepped: 'middle',
        },
        {
            label: '2023',
            data: [29,30,32,32,32,32,32,32,34,36,34,35],
            fill: false,
            stepped: 'middle',
        },
        {
            label: '2024',
            data: [35,35,,,,,,,,,,],
            fill: false,
            stepped: 'middle',
        }        
  ]
},
options: {
    maintainAspectRatio: false,
    animations: animation,
    onClick: (event, elements, chart) => {
      chart.stop();
      chart.update();
    }
}
{{< /chart >}}
<!-- prettier-ignore-end -->
