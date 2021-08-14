---
title: 整合架構延伸與消費者介面
description: Active Directory Domain Services 的管理工具使用通用的架構，將系統管理使用者介面連接到目錄架構。
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d951ec51d7453ee92cf90ddcb28ddb8219d3056b1edb96d16bf15494fe956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187207"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>整合架構延伸與消費者介面

Active Directory Domain Services 的管理工具使用通用的架構，將系統管理使用者介面連接到目錄架構。 此架構的文字核心是 **displaySpecifier** 物件類別。 在 [擴充目錄物件的消費者介面](extending-the-user-interface-for-directory-objects.md)時，會詳細說明顯示規範及其用法。

當您藉由子類別化現有類別來建立新類別時，您可以藉由複製超級類別的顯示規範來利用超類別的現有 UI。 複製類別的顯示規範的簡單方式，就是使用 LDIFDE 將它匯出至 LDIF 檔案、編輯辨別名稱和 CN，然後匯入修改過的 LDIF 檔案。 如果子類別具有其他屬性，您將需要提供額外的屬性頁來支援編輯。 如果子類別具有其他的必須具有屬性，您就必須提供建立對話方塊延伸頁面，因為超級類別提供的 UI 無法建立這些新屬性。

 

 




