---
description: 電話物件是代表實際電話裝置及其所有控制項的實體。
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: 電話物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981188"
---
# <a name="phone-object-interfaces"></a>電話物件介面

電話物件是代表實際電話裝置及其所有控制項的實體。

[**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)和 [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)介面不會直接在 Phone 物件上公開，但與其緊密相關，並在此處列出以方便參考。



| 介面                                                  | 描述                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | 允許存取電話裝置，其層級可與 TAPI 2 所提供的相同。*x* C API。                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | 提供的方法可讓您自動控制手機的聲音和環形，以及根據手機的 hookswitch 狀態進行自動通話處理。 |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | 抓取電話事件的描述。                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | 列舉 [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)。                                                                                                    |



 

 

 



