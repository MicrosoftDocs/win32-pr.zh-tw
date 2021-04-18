---
title: Windows 動畫工作
description: 本節所包含的主題說明使用 Windows 動畫管理員的應用程式所需的基本工作。
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Windows 動畫視窗動畫，工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965812"
---
# <a name="windows-animation-tasks"></a>Windows 動畫工作

本節所包含的主題說明使用 Windows 動畫管理員的應用程式所需的基本工作。

這些工作（依順序）包括：

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                | 描述                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [建立主要動畫物件](adding-animation-to-an-application.md)<br/>               | 若要在您的應用程式中使用 Windows 動畫，第一個步驟就是建立一組小型的主要動畫物件。<br/>                                                                                                                                                                           |
| [建立動畫變數](create-animation-variables.md)<br/>                              | 應用程式必須針對每個要使用 Windows 動畫製作動畫的視覺特性建立動畫變數。<br/>                                                                                                                                                            |
| [更新動畫管理員並繪製畫面格](introducing-windows-animation-manager.md)<br/> | 每次應用程式排程分鏡腳本時，應用程式都必須提供目前的時間給動畫管理員。 當您導向動畫管理員以更新其狀態，並將所有動畫變數設定為適當的插入值時，也需要目前的時間。<br/> |
| [讀取動畫變數值](updating---application-driven-animation.md)<br/>         | 每次您的應用程式繪製時，都應該讀取代表要進行動畫之視覺特性的動畫變數目前的值。<br/>                                                                                                                                  |
| [建立分鏡腳本並新增轉換](updating---timer-driven-animation.md)<br/>          | 若要建立動畫，應用程式必須建立分鏡腳本。<br/>                                                                                                                                                                                                                        |
| [排程分鏡腳本](scheduling-a-storyboard.md)<br/>                                      | 建立分鏡腳本之後，動畫管理員會進行排程。<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 動畫總覽](scenic-animation-api-overview.md)
</dt> <dt>

[Windows 動畫參考](windows-animation-reference.md)
</dt> <dt>

[Windows 動畫範例](windows-animation-samples.md)
</dt> </dl>

 

 





