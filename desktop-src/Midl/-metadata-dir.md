---
title: '/metadata_dir 切換 (MIDLRT.EXE 根據) '
description: /Metadata \_ dir 參數指定一或多個包含平臺中繼資料檔案的目錄。
ms.assetid: 578b9d3f-3ee6-4978-9d2a-0c5aee561a30
keywords:
- /metadata_dir switch MIDL
topic_type:
- apiref
api_name:
- /metadata_dir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72781641323aa61ae75da256f84f8c1debfd6556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978469"
---
# <a name="metadata_dir-switch-midlrt"></a>/metadata_dir 切換 (MIDLRT.EXE 根據) 

**/Metadata \_ dir** 參數指定一或多個包含平臺中繼資料檔案的目錄。

``` syntax
midlrt /metadata_dir metadata_directory
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*中繼資料 \_ 目錄* 
</dt> <dd>

指定包含平臺中繼資料檔案的一或多個目錄。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用這個參數來指定 Windows 的主要中繼資料檔案的位置，該檔案的名稱為 windows. winmd。

## <a name="examples"></a>範例

**midlrt.exe 根據/metadata \_ dir dir1 dir2**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------|
| 用戶端<br/> | Windows 8<br/>           |
| 伺服器<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





