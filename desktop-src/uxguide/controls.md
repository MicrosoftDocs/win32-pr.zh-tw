---
title: '控制 (設計基本概念) '
description: 控制項是使用者在應用程式主視窗區域上與使用者互動的 UI 元素。 查看以 Windows 為基礎的桌面應用程式中控制項的視覺範例，並取得每個控制項的指導方針連結。
ms.assetid: 5c48728b-6d86-4827-9757-f06c23ca54d8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c44e7b5f3772984b1dc24b166b9fe8c03a395f8a
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524312"
---
# <a name="controls-design-basics"></a>控制 (設計基本概念) 

> [!NOTE]
> 此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。 大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。

控制項是使用者在應用程式主視窗區域上與使用者互動的 UI 元素。 查看以 Windows 為基礎的桌面應用程式中控制項的視覺範例，並取得每個控制項的指導方針連結。



|          範例                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![氣球](images/controls-image1.png)<br/> [批註](ctrl-balloons.md) 提示使用者在控制項中通知使用者非重大問題或特殊狀況。<br/>                                                                                                                                                                                                                 |
| ![相應](images/controls-image2.png)<br/> [核取方塊](ctrl-check-boxes.md) 可讓使用者在兩個或多個明顯不同的選項之間做出決定。<br/>                                                                                                                                                                                                     |
| ![命令按鈕](images/controls-image3.png)<br/> [命令按鈕](ctrl-command-buttons.md) 可讓使用者執行立即動作。<br/>                                                                                                                                                                                                                         |
| ![命令連結](images/controls-image4.png)<br/> [命令連結](ctrl-command-links.md) 可讓使用者在一組互斥、相關的選項之間做出選擇。<br/>                                                                                                                                                                                          |
| ![下拉式方塊和下拉式方塊](images/controls-image5.png)<br/> [下拉式清單和下拉式方塊](/windows/desktop/uxguide/ctrl-drop) 可讓使用者在互斥值清單中進行選擇。<br/>                                                                                                                                                                           |
| ![群組方塊](images/controls-image6.png)<br/> [群組方塊](ctrl-group-boxes.md) 可讓使用者查看一組相關控制項之間的關聯性。<br/>                                                                                                                                                                                                                |
| ![連結](images/controls-image7.png)<br/> [連結](ctrl-links.md) 可讓使用者流覽至另一個頁面、視窗或說明主題;顯示定義;起始命令;或選擇選項。<br/>                                                                                                                                                                    |
| ![清單方塊](images/controls-image8.png)<br/> [清單方塊](ctrl-list-boxes.md) 可讓使用者從清單中顯示且一律可見的一組值進行選取。 使用單一選取清單方塊時，使用者會從互斥值清單中選取一個專案。 使用多重選取清單方塊時，使用者會從值清單中選取零個以上的專案。<br/> |
| ![清單視圖](images/controls-image9.png)<br/> [清單視圖](ctrl-list-views.md) 可讓使用者使用單一選取或多重選取專案來查看資料物件的集合，並與之互動。<br/>                                                                                                                                                           |
| ![通知](images/controls-image10.png)<br/> [通知](mess-notif.md) 會通知使用者與目前使用者活動不相關的事件。<br/>                                                                                                                                                                                                          |
| ![進度列](images/controls-image11.png)<br/> [進度](progress-bars.md) 列可讓使用者追蹤長時間操作的進度。<br/>                                                                                                                                                                                                                    |
| ![漸進式洩漏](images/controls-image12.png)<br/> [漸進式洩漏控制項](ctrl-progressive-disclosure-controls.md) 可讓使用者顯示或隱藏其他資訊，包括資料、選項或命令。<br/>                                                                                                                                   |
| ![選項按鈕](images/controls-image13.png)<br/> [選項按鈕](ctrl-radio-buttons.md) 可讓使用者在一組互斥、相關的選項之間做出選擇。<br/>                                                                                                                                                                                         |
| ![搜尋方塊](images/controls-image14.png)<br/> [搜尋方塊](ctrl-search-boxes.md) 可讓使用者快速找出特定的物件或文字。<br/>                                                                                                                                                                                                              |
| ![滑桿](images/controls-image15.png)<br/> [滑杆](ctrl-sliders.md) 可讓使用者從連續的值範圍中選擇。<br/>                                                                                                                                                                                                                                   |
| ![自 旋](images/controls-image16.png)<br/> [微調控制項](ctrl-spin-controls.md) 可讓使用者以累加方式變更其相關聯數值文字方塊內的值。<br/>                                                                                                                                                                                            |
| ![狀態列](images/controls-image17.png)<br/> [狀態列](ctrl-status-bars.md) 會顯示目前視窗狀態、背景工作或其他內容資訊的相關資訊。<br/>                                                                                                                                                                  |
| ![索引標籤](images/controls-image18.png)<br/> 索引標籤[會顯示使用者](ctrl-tabs.md)有關個別標記頁面的相關資訊。<br/>                                                                                                                                                                                                                                   |
| ![文字方塊](images/controls-image19.png)<br/> [文字方塊](ctrl-text-boxes.md) 可讓使用者顯示、輸入或編輯文字或數值。<br/>                                                                                                                                                                                                                    |
| ![提示](images/controls-image20.png)<br/> [工具提示](ctrl-tooltips-and-infotips.md) 會標示未標記的控制項。<br/>                                                                                                                                                                                                                                                |
| ![提示](images/controls-image21.png)<br/> [提示](ctrl-tooltips-and-infotips.md) 描述使用者所指向的物件。<br/>                                                                                                                                                                                                                          |
| ![treeview](images/controls-image22.png)<br/> [樹狀檢視](ctrl-tree-views.md) 可讓使用者使用單一選取或多重選取專案，來查看階層式排列的物件集合，並與其互動。<br/>                                                                                                                                        |



 

