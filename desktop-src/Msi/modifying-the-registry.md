---
description: 當所有選取的元件及其相關檔案都已安裝之後，就可以將登錄機碼寫入系統登錄。
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: 修改登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f1bd6145811097fcaf74f0622ac35412891d6aa0007c4411099ade6afddd36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082858"
---
# <a name="modifying-the-registry"></a>修改登錄

當所有選取的元件及其相關檔案都已安裝之後，就可以將登錄機碼寫入系統登錄。 與修改登錄相關的標準動作必須在檔案安裝標準動作之後進行排序，因為除非已成功安裝對應的元件和檔案，否則無法寫入登錄機碼。

[RegisterClassInfo 動作](registerclassinfo-action.md)會存取[類別資料表](class-table.md)，以註冊已安裝元件的 COM 類別資訊。

[RegisterExtensionInfo 動作](registerextensioninfo-action.md)會查詢[延伸模組資料表](extension-table.md)和[動詞資料表](verb-table.md)，並向作業系統註冊對應的擴充功能和命令動詞資訊。

[RegisterProgIdInfo 動作](registerprogidinfo-action.md)會管理 OLE ProgId 資訊與作業系統的註冊。

[RegisterMIMEInfo 動作](registermimeinfo-action.md)會處理[mime 資料表](mime-table.md)，以註冊 mime 內容類型、副檔名和 CLSID 之間的關聯。

[WriteRegistryValues 動作](writeregistryvalues-action.md)會處理登錄[表](registry-table.md)，並寫入已安裝在本機或從來源執行之所有元件的金鑰。 登錄資料表可讓您將金鑰寫入 **HKEY \_ 類別 \_ ROOT**、 **HKEY \_ CURRENT \_ USER**、 **HKEY \_ LOCAL \_ MACHINE** 和 **HKEY \_ USERS** Registry hive。

[RemoveRegistryValues 動作](removeregistryvalues-action.md)會移除已標示為要在登錄[資料表](registry-table.md)的 [名稱] 資料行或[RemoveRegistry 資料表](removeregistry-table.md)中刪除的索引鍵。

[RegisterTypeLibraries 動作](registertypelibraries-action.md)會處理[TypeLib 資料表](typelib-table.md)，並向系統註冊已安裝的類型程式庫。

 

 



