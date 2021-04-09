---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: 與 HKEY \_ 本機電腦軟體類別機碼相關聯的子機碼與登錄值， \_ \\ \\ 包含支援 COM 功能所需之應用程式的相關資訊。
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675599"
---
# <a name="hkey_local_machinesoftwareclasses"></a>HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別

與 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別機** 碼相關聯的子機碼與登錄值，包含支援 COM 功能所需之應用程式的相關資訊。 此資訊包括支援的資料格式、相容性資訊、程式設計識別碼、DCOM 和控制項等主題。



| 子機碼                                                                         | Description                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid-key.md)                                                     | 以 COM 為基礎之應用程式的設定選項。                                                                 |
| [**Clsid**](clsid-key-hklm.md)                                                | COM 類別的設定選項。                                                                            |
| [**<\_ 副檔名>**](-file-extension--key.md)                        | 將副檔名與 ProgID 產生關聯。                                                                   |
| [**FileType**](filetype-key.md)                                               | [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)用來比對非複合檔案中各種檔案位元組的模式。 |
| [**介面**](interface-key.md)                                             | 將介面名稱與介面識別碼 (IID) 相關聯。                                                          |
| [**<ProgID>**](-progid--key.md)                                         | 識別類別。 請注意，ProgID 不保證是全域唯一的，與 CLSID 不同。                 |
| [**<與版本無關的 ProgID>**](-version-independent-progid--key.md) | 用來判斷物件應用程式的最新版本。                                                    |



 

 

 




