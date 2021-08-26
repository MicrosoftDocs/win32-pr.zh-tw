---
title: 選擇描述性屬性的內容
description: 某些屬性的內容是特定的，而其他屬性的內容則是由伺服器開發人員所提供的描述性文字所組成。
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5215a6592d11272223654184340c4df8b299b88edb5b5f4addbd2c8d4712ab74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071848"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>選擇描述性屬性的內容

某些屬性的內容是特定的，而其他屬性的內容則是由伺服器開發人員所提供的描述性文字所組成。 此外，每個屬性的資訊類型都會根據物件而有所不同。 下表提供選擇這些描述性屬性內容的建議。



| 屬性                                        | 內容建議                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**名稱**](name-property.md)                   | 此標籤會在其容器內簡短描述和識別物件，例如按下按鈕中的文字、功能表項目的名稱，或是在編輯控制項旁邊顯示的標籤。                                                                              |
| [**DefaultAction**](defaultaction-property.md) | 與物件的預設互動。 這個屬性所傳回的字串是單一動詞，例如，針對工具列按鈕按下 "，或以動詞開頭的簡短片語。                                                                               |
| [**值**](value-property.md)                 | 物件中包含的資訊，例如編輯控制項中的文字或 HTML 連結的檔案名。 [**Value**](value-property.md)屬性的內容可以變更，而 [**Name**](name-property.md)屬性的內容不會變更。 |
| [**描述**](description-property.md)     | 描述物件的外觀。                                                                                                                                                                                                                                    |
| [**説明**](help-property.md)                   | 工具提示或氣球樣式的資訊，用來描述物件的用途或使用方式。                                                                                                                                                                   |
| [**HelpTopic**](helptopic-property.md)         | 檔物件之 [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) 主題的內容識別碼。                                                                                                                                                 |



 

針對 [**角色**](role-property.md)使用其中一個預先定義的 [物件角色](object-roles.md)值，並針對該 [**狀態**](state-property.md)使用適當的 [物件狀態常數](object-state-constants.md)組合。

自訂控制項的屬性內容必須符合自訂控制項所模擬之系統提供控制項的屬性內容。 如需系統提供之控制項所支援之屬性的詳細資訊，請參閱 [附錄 A：支援的消費者介面專案參考](appendix-a--supported-user-interface-elements-reference.md)。

 

 