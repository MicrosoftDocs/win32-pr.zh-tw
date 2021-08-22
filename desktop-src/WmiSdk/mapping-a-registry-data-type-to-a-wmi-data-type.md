---
description: 應用程式必須建立具有對應至登錄資料類型之資料類型的屬性。
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: 將登錄資料類型對應至 WMI 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e620d51eee52592df946e822165d8ed1833214c6f75519d4274b0d7fe3f5550c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050686"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>將登錄資料類型對應至 WMI 資料類型

應用程式必須建立具有對應至登錄資料類型之資料類型的屬性。 您不需要在建立、取得或設定登錄值的方法中指定登錄資料類型。 但是，包含值的輸入參數必須是正確的 WMI 資料類型。 例如，如果應用程式從登錄接收 **REG \_ DWORD** 資料，則接收資料的類別必須包含 **Uint32** 屬性。

下表列出 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 方法中所使用之登錄和 WMI 資料類型之間的對應。



| 登錄資料類型      | WMI 資料類型                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **REG \_ 二進位檔**         | **uint8** 陣列<br/> 值的陣列，這些值不超過255或 hex FF。 例如，下列 Visual Basic 腳本程式碼會建立符合此資料類型的陣列。<br/> `BinArray = Array(&H01, &Ha2)`<br/> [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別方法 [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)需要 **REG \_ BINARY** 資料類型。<br/>                                                                                          |
| **REG \_ DWORD**          | **uint32**、 **sint32** 或 Visual Basic **整數**<br/> 單一32位值。 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別方法 [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)和 [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)需要 **REG \_ DWORD** 資料類型。<br/>                                                                                                                                                                  |
| **REG \_ SZ**             | **string**<br/> [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別方法 [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)需要 **REG \_ SZ** 資料類型。<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **uint64**。<br/> 單一64位值。 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別方法 [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov)和 [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov)需要 **REG \_ QWORD** 資料類型。<br/>                                                                                                                                                                                                         |
| **REG \_ EXPAND \_ SZ**     | **string**<br/> 展開的字串是代表系統內容變數的特殊字元串。 例如，下列 VBScript 程式碼會建立代表 **HKEY \_ 本機 \_ 使用者** 環境變數 TEMP 的字串。<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別方法 [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov)需要 **REG \_ EXPAND \_ SZ** 資料類型。<br/> |
| **REG \_ 多重 \_ SZ**      | **字串** 陣列<br/> Multistring 資料類型包含多個字串。 例如，下列 VBScript 程式碼會建立符合此資料類型的陣列。<br/> `MultiValue = Array("first", "second", "third")`<br/> [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別方法 [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)需要 **REG \_ 多重 \_ SZ** 資料類型。<br/>                                                                     |
| **REG \_ 資源 \_ 清單** | 視需要。 如需詳細資訊，請參閱描述登錄的 [資源](describing-a-resource-for-the-registry.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[定義 System Registry 提供者的類別](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

