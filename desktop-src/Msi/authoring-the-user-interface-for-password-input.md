---
description: 針對每個必須由使用者輸入的密碼，在儲存密碼值的對話方塊上新增編輯控制項至屬性。
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: 撰寫密碼輸入的消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971752"
---
# <a name="authoring-the-user-interface-for-password-input"></a>撰寫密碼輸入的消費者介面

針對每個必須由使用者輸入的密碼，在儲存密碼值的對話方塊上新增編輯控制項至屬性。 此 [編輯控制項](edit-control.md) 應具有 [密碼控制項屬性](password-control-attribute.md)。 這會指定輸入的屬性為密碼，並防止安裝程式將屬性寫入記錄檔。

密碼編輯控制項的 [控制項屬性](control-attributes.md) 為 MsidbControlAttributesVisible、MsidbControlAttributesEnabled 和 msidbControlAttributesPasswordInput (1 + 2 + 2097152) 。 X、Y、寬度、高度和控制項 \_ 下一步取決於對話方塊上控制項的版面配置。

[控制資料表](control-table.md)



| 對話\_ | 控制項\_            | 類型 | X   | Y   | 寬度 | 高度 | 屬性 | 屬性         | Text | 控制 \_ 下一步 | Help |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordEdit | 編輯 | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | 取消        |      |



 

繼續 [保護安裝的安全](securing-the-installation.md)。

 

 



