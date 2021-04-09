---
description: 定義標準、特定和一般許可權。 這些許可權用於 (Ace 的存取控制專案) ，而且是指定要求或授與物件之存取權的主要方式。
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: 'ACCESS_MASK (Winnt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115333"
---
# <a name="access_mask"></a>存取 \_ 遮罩

**存取 \_ 遮罩** 資料類型是一種 **DWORD** 值，可定義標準、特定和一般許可權。 這些許可權用於 (Ace 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)) ，而且是指定要求或授與物件之存取權的主要方式。


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>備註

此值的位配置如下。



| Bits             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | 特定權利。 包含與遮罩相關聯之物件類型的特定存取遮罩。<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | 標準權利。 包含物件的標準存取權限。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | 存取系統安全性 (**存取 \_ 系統 \_ 安全性**) 。 它是用來指出 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) 存取權。 這種類型的存取需要呼叫進程擁有 **SE \_ 安全性 \_ 名稱** (管理審核和安全性記錄) 許可權。 如果在 audit access ACE 的存取遮罩中設定這個旗標 (成功或失敗的存取) ，則會審核 SACL 存取。<br/> |
| 25<br/>    | 允許的最 **大 \_ ()** 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | 保留的。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | 泛型所有 (**一般 \_ 都** 是) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | 一般執行 (**一般 \_ 執行**) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | 一般寫入 (**一般 \_ 寫入**) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | 泛型讀取 (**一般 \_ 讀取**) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

標準許可權位（16到23）包含物件的標準存取權限，而且可以是下列預先定義旗標的組合。



| bit           | 旗標                         | 意義                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | 刪除存取權。<br/>                                                                                                                                                                                                                |
| 17<br/> | **讀取 \_ 控制**<br/> | 擁有者、群組和 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 的讀取權限 (DACL) 的安全描述項。<br/> |
| 18<br/> | **寫入 \_ DAC**<br/>    | DACL 的寫入權限。<br/>                                                                                                                                                                                                     |
| 19<br/> | **寫入 \_ 擁有者**<br/>  | 擁有者的寫入權限。<br/>                                                                                                                                                                                                        |
| 20<br/> | **同步**<br/>   | 同步存取。<br/>                                                                                                                                                                                                           |



 

在 Winnt 中定義的下列常數表示特定和標準存取權限。


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Winnt (包括 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[存取控制](access-control.md)
</dt> <dt>

[基本存取控制結構](authorization-structures.md)
</dt> <dt>

[存取權限和存取遮罩](access-rights-and-access-masks.md)
</dt> <dt>

[**泛型 \_ 對應**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

