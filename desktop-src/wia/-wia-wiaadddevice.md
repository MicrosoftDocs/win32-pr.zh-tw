---
description: WiaAddDevice 函式會叫用掃描器和相機安裝精靈 UI。 它相當於執行 &\# 0034; rundll32.exe sti \_ci.dll AddDevice&\# 0034; 從命令提示字元。
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: 'WiaAddDevice 函式 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 81dcff3cdca3459126751b12b86f1e11adc2b4fec8926f69211f0508253b64fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965397"
---
# <a name="wiaadddevice-function"></a>WiaAddDevice 函式

**WiaAddDevice** 函式會叫用掃描器和相機安裝精靈 UI。 這相當於從命令提示字元執行 "rundll32.exe sti \_ci.dll AddDevice"。

## <a name="syntax"></a>語法


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函式應以系統管理員認證來呼叫。 在 [使用者帳戶控制] 下執行 (LUA) 時，應提高處理常式的許可權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




