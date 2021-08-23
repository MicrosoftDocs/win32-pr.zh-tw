---
description: 結束非活動狀態的監視。
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: EndIdleDetection 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: a2ba6732b9221d4d4d43e670d0d42d39363d50dffc0d2d4b0daf378b10dd292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691408"
---
# <a name="endidledetection-function"></a>EndIdleDetection 函式

\[這項功能不受支援，而且可能會在未來變更或無法使用。 請改用 **GetLastInputInfo** 函數。\]

結束非活動狀態的監視。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>dwreserved* 
</dt> <dd>

此參數必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。 此函式不是依名稱匯出;呼叫 **GetProcAddress** 時指定序數4。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
