---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682412"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Text

這個元素似乎是 tabbable，但不在定位順序中。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

您無法使用標準鍵盤流覽 (Tab 或 Shift + Tab) 來存取可設定焦點的元素。 例如，元素未標示為定位停駐點或指派索引標籤索引。 此問題會造成依賴螢幕讀取器和鍵盤進行流覽的人員發生問題，原因如下：

-   元素無法探索。
-   如果元素是自訂清單控制項的子系，則表示可以使用箭號或頁面索引鍵來導覽子項目的提示可能會遺失。

## <a name="possible-causes"></a>可能的原因

-   未正確設定元素或其父系的 MSAA 角色。 例如，如果清單視圖控制項中的所有清單專案都不會透過 MSAA 以角色系統專案識別碼公開 \_ \_ ，驗證就會失敗，因為無法使用 Tab 鍵來存取清單專案。
-   元素或其父代是未正確執行 tab 鍵的自訂控制項。 例如，[MSAA 狀態] 屬性永遠不會設定為 [狀態 \_ 系統可 \_ 設定]。
-   做為其他元素之容器的專案，已選取要進行驗證，但不支援鍵盤流覽本身。 例如，無法使用 TAB 鍵來存取工具列和其子項目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[鍵盤使用者介面設計指導方針](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 