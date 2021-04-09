---
title: MirrorIcon 函式
description: 反轉 (鏡像) 圖示，使其在鏡像裝置內容上正確顯示。
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- MirrorIcon 函式 Windows 控制項
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024725"
---
# <a name="mirroricon-function"></a>MirrorIcon 函式

\[**MirrorIcon** 可透過 Windows XP Service Pack 2 (SP2) 取得。 它可能會在後續版本中變更或無法使用。\]

反轉 (鏡像) 圖示，使其在鏡像裝置內容上正確顯示。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phIconSmall* \[in、out、optional\]
</dt> <dd>

類型： **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

圖示控制碼的指標，該控制碼會參考小版本的圖示。

</dd> <dt>

_phIconLarge * \[ in、out、optional\]
</dt> <dd>

類型： **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

圖示控制碼的指標，參考大型版本的圖示。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)**

如果成功，則 **為 TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

**MirrorIcon** 不會依名稱匯出，也不會在公用標頭檔中宣告。 若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數414來取得函式指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (5.81 版或更新版本) </dt> </dl> |



 

