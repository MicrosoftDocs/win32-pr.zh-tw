---
description: 從登錄重載色彩設定。
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989798"
---
# <a name="frefreshstyle-function"></a>FRefreshStyle 函式

從登錄重載色彩設定。

## <a name="syntax"></a>語法


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

成功時傳回 TRUE;否則為 FALSE。

## <a name="remarks"></a>備註

此函式與匯入程式庫或標頭檔沒有關聯;您必須使用 [**LoadLibrary**](-loadlibrary.md) 和 [**GetProcAddress**](-getprocaddress-.md) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




