---
description: 表示當做引數使用的路徑類型。
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: PATH_TYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c05e71e485eaaf3ff309dc3a0df3d792ccd18c1438964d387afe969adbfd3fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058598"
---
# <a name="path_type-enumeration"></a>路徑 \_ 類型列舉

表示當做引數使用的路徑類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**DOS \_ 路徑**
</dt> <dd>

標準路徑。

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**NT \_ 路徑**
</dt> <dd>

內部路徑。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




