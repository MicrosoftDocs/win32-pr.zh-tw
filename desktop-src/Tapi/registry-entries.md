---
description: 可插入的終端會分類為終端超類。
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: " (電話語音 API) 的登錄專案"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976374"
---
# <a name="registry-entries-telephony-api"></a> (電話語音 API) 的登錄專案

可插入的終端會分類為終端超類。 在登錄中，每個終端超級類別都有下列機碼專案：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **電話語音** \\ **TerminalManager**

在終端超級類別下，終端超級類別機碼為終端超級類別內每個可插入終端機的專案。

每個終端超級類別的專案都是由終端超級類別 CLSID 所識別。 這是終端機類別的唯一識別碼。 終端機類別具有選擇性的屬性：名稱，這是終端機類別的易記名稱。 每個可插入的終端機都是由 CLSID 終端機類別來識別;亦即 GUID。 插即用終端機的屬性會儲存至可插入的終端機碼值。 插入式終端機的屬性如下所示。



| Terminal 類別 | 索引鍵名稱 | 公用識別碼                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Name           | REG \_ SZ  | 終端機易記名稱                                                            |
| 公司        | REG \_ SZ  | 公司名稱                                                                      |
| 版本        | REG \_ SZ  | 版本資訊                                                               |
| CLSID          | REG \_ SZ  | COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法中使用的終端機 CLSID ()  |
| 方向     | DWORD    | 終端機方向                                                                |
| MediaTypes     | DWORD    | 支援的終端媒體類型                                                    |



 

終端機類別的屬性如下所示。



| CLSID | 索引鍵名稱 | 公用識別碼            |
|-------|----------|------------------------------|
| Name  | REG \_ SZ  | 終端機類別易記名稱 |



 

 

 
