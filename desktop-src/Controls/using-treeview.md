---
title: 使用 Tree-View 控制項
description: 本章節包含使用樹狀檢視控制項的執行詳細資料與範例程式碼。
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9ed8d1040a635964e772b8399a5c476e67f9aba
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965674"
---
# <a name="using-tree-view-controls"></a>使用 Tree-View 控制項

本章節包含使用樹狀檢視控制項的執行詳細資料與範例程式碼。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [如何建立 Tree-View 控制項](create-a-tree-view-control.md)<br/>       | 若要建立樹狀檢視控制項，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，指定 window 類別的 [**WC \_ TREEVIEW**](common-control-window-classes.md) 值。 載入通用控制項 DLL 時，會在應用程式的位址空間中註冊樹狀檢視視窗類別。 若要確定已載入 DLL，請使用 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 函數。 <br/>                                                                    |
| [如何初始化影像清單](initialize-the-image-list.md)<br/>         | 樹狀檢視控制項中的每個專案都可以有兩個相關聯的影像。 專案會在選取時顯示一個影像，另一個則不會顯示。 若要包含具有樹狀檢視專案的影像，請先使用 [影像](image-lists.md) 清單函式來建立影像清單，並在其中新增影像。 然後使用 [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) 訊息，將影像清單與樹狀檢視控制項產生關聯。 <br/>                                                                     |
| [如何新增 Tree-View 專案](add-tree-view-items.md)<br/>                     | 您可以藉由將 [**TVM \_ INSERTITEM**](tvm-insertitem.md) 訊息傳送至控制項，將專案加入至樹狀檢視控制項。 訊息包含 [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) 結構的位址，指定父專案、插入新專案之後的專案，以及定義專案屬性的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) 結構。 這些屬性包括專案的標籤、其選取的和 nonselected 的影像，以及32位的應用程式定義值。 <br/> |
| [如何拖曳 Tree-View 專案](drag-a-tree-view-item.md)<br/>                 | 本主題將示範處理樹狀檢視專案的拖放程式碼。 範例程式碼是由三個函式所組成。 第一個函式會開始拖曳作業，第二個函式會拖曳影像，而第三個函式會結束拖曳作業。 <br/>                                                                                                                                                                                                                                  |
| [如何使用狀態影像索引](work-with-state-image-indexes.md)<br/> | 通常會對如何在樹狀檢視控制項中設定和取出狀態影像索引產生混淆。 下列範例示範設定和抓取狀態影像索引的適當方法。 這些範例假設樹狀檢視控制項中只有兩個狀態影像索引，未核取並核取。 如果您的應用程式包含兩個以上的應用程式，則必須修改這些函式來處理該案例。 <br/>                                                               |
| [如何使用 Tree-View 提示](use-tree-view-infotips.md)<br/>               | 當您將 [**電視資料 \_**](tree-view-control-window-styles.md) 提示樣式套用至樹狀檢視控制項時，當游標位於樹狀檢視中的專案上方時，它會產生 [izdebski \_ GETINFOTIP](tvn-getinfotip.md) 通知。 藉由回應此通知，您可以設定出現在提示中的文字。 <br/>                                                                                                                                                                                    |



 

 

