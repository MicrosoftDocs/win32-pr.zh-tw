---
description: 開始監視非活動狀態。
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 1bbb27114177a6f64f471b0122832bc09180988019bc23a63343920eb76221f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002318"
---
# <a name="beginidledetection-function"></a>BeginIdleDetection 函式

\[這項功能不受支援，而且可能會在未來變更或無法使用。 請改用 **GetLastInputInfo** 函數。\]

開始監視非活動狀態。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfnCallback* 
</dt> <dd>

當閒置狀態變更時所呼叫的函數。 此回呼的定義如下：

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*dwIdleMin* 
</dt> <dd>

對回呼函式進行呼叫之前的非活動分鐘數。

</dd> <dt>

*>dwreserved* 
</dt> <dd>

此參數必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 0;否則，它會傳回錯誤碼。 例如，如果 *>dwreserved* 是0以外的任何一項，則會傳回 **錯誤的 \_ \_ 資料無效** 。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。 此函式不是依名稱匯出;呼叫 **GetProcAddress** 時指定序數3。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
