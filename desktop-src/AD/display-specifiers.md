---
title: 顯示規範
description: 在 Active Directory Domain Services 中，物件類別或類別會定義可在 Active Directory Domain Services 中建立的物件類型。
ms.assetid: 0c31b02b-9fd3-4547-9ebc-d511a10d7106
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be9df0b81427bafa6ebe6707a33e86b6aff7416
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933079"
---
# <a name="display-specifiers"></a>顯示規範

在 Active Directory Domain Services 中，物件類別或類別會定義可在 Active Directory Domain Services 中建立的物件類型。 每個物件類別的定義會以 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 物件的形式儲存在 [Active Directory 架構](active-directory-schema.md)中。 除了 **classSchema** 定義之外，每個物件類別都可以有一個或多個顯示指定名稱，以指定該類別物件的使用者介面資料。

顯示規範是 [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) 類別的物件。 **DisplaySpecifier** 物件的屬性會指定當地語系化的使用者介面資料，以描述特定物件類別的各種 UI 元素。 顯示規範：儲存屬性工作表、內容功能表、圖示、建立嚮導和當地語系化類別和屬性名稱的資料。 針對屬性頁和內容功能表，Windows shell 和 Active Directory 系統管理嵌入式管理單元會使用此資料來為系統管理員和使用者形成不同的使用者介面，一組屬性頁和/或內容功能表可以與系統管理應用程式產生關聯，而一組不同的專案可以與使用者應用程式產生關聯。

[**DisplaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier)物件會儲存在設定容器中 DisplaySpecifiers 容器內的地區設定專屬容器中，該容器會複寫至企業樹系中的每個網域控制站。 DisplaySpecifiers 容器具有對應至企業安裝所支援之各種地區設定的子容器。 這些子容器會使用語言識別項來命名。 例如，US-English 的地區設定容器名稱是409，這會對應至十六進位語言識別項0x0409。 因此，物件類別可以有多個顯示規範：每個地區設定 subcontainer 一個。 如需詳細資訊和可能的語言識別項清單，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。 如需地區設定的詳細資訊，請參閱 [地區設定和語言](/windows/desktop/Intl/locales-and-languages)。

[**DisplaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier)物件的名稱是藉由將字串 "-Display" 附加至物件類別的 [**lDAPDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname)來形成。 例如，[**使用者**](/windows/desktop/ADSchema/c-user)類別的 **displaySpecifier** 物件名稱是「使用者-顯示」。

您可以新增、刪除或修改類別 [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) 物件的屬性，以指定 UI 元素 (類別名稱、屬性名稱、屬性工作表、內容功能表、圖示等) 出現在該類別之物件的每個實例上。

如需顯示規範的詳細資訊，請參閱 [DisplaySpecifiers 容器](displayspecifiers-container.md)。

 

 