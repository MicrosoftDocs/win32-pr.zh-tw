---
title: Windows動畫工作
description: 本節所包含的主題描述使用 Windows 動畫管理員的應用程式所需的基本工作。
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Windows動畫 Windows 動畫、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8f5116a6e36697e649ad81bfbad883c57aee50440c3ba80734419ce2fb372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058146"
---
# <a name="windows-animation-tasks"></a>Windows動畫工作

本節所包含的主題描述使用 Windows 動畫管理員的應用程式所需的基本工作。

這些工作（依順序）包括：

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                | 描述                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [建立主要動畫物件](adding-animation-to-an-application.md)<br/>               | 若要在您的應用程式中使用 Windows 動畫，第一個步驟是建立一組小型的主要動畫物件。<br/>                                                                                                                                                                           |
| [建立動畫變數](create-animation-variables.md)<br/>                              | 應用程式必須針對每個要使用 Windows 動畫進行動畫的視覺特性，建立動畫變數。<br/>                                                                                                                                                            |
| [更新動畫管理員並繪製畫面格](introducing-windows-animation-manager.md)<br/> | 每次應用程式排程分鏡腳本時，應用程式都必須提供目前的時間給動畫管理員。 當您導向動畫管理員以更新其狀態，並將所有動畫變數設定為適當的插入值時，也需要目前的時間。<br/> |
| [讀取動畫變數值](updating---application-driven-animation.md)<br/>         | 每次您的應用程式繪製時，都應該讀取代表要進行動畫之視覺特性的動畫變數目前的值。<br/>                                                                                                                                  |
| [建立分鏡腳本並新增轉換](updating---timer-driven-animation.md)<br/>          | 若要建立動畫，應用程式必須建立分鏡腳本。<br/>                                                                                                                                                                                                                        |
| [排程分鏡腳本](scheduling-a-storyboard.md)<br/>                                      | 建立分鏡腳本之後，動畫管理員會進行排程。<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows動畫總覽](scenic-animation-api-overview.md)
</dt> <dt>

[Windows動畫參考](windows-animation-reference.md)
</dt> <dt>

[Windows動畫範例](windows-animation-samples.md)
</dt> </dl>

 

 





