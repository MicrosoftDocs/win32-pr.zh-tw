---
title: 'MCI_MAKE_MSF 宏 (Mciapi) '
description: MCI \_ 讓 \_ msf 宏在指定的分鐘數、秒數和框架值中，以壓縮的分鐘/秒/框架來建立時間值 (MSF) 格式。
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f5cfa2b99f7bdbd7eb3029b3f0186904d8b8e94f455614464fadc98cdd20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690128"
---
# <a name="mci_make_msf-macro"></a>MCI \_ MAKE \_ MSF 宏

**MCI \_ 讓 \_ msf** 宏在指定的分鐘數、秒數和框架值中，以壓縮的分鐘/秒/框架來建立時間值 (MSF) 格式。

## <a name="syntax"></a>語法


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*分鐘* 
</dt> <dd>

分鐘數。

</dd> <dt>

*seconds* 
</dt> <dd>

秒數。

</dd> <dt>

*框架* 
</dt> <dd>

畫面格數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回壓縮 MSF 格式的時間。

## <a name="remarks"></a>備註

MSF 格式的時程表示為 **DWORD** 值，具有最小的最小位元組數（包含分鐘）、下一個最不重要的位元組（包含秒），以及下一個包含框架的最小有效位元組。 最重要的位元組未使用。

**MCI \_ MAKE \_ MSF** 巨集定義如下：


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mciapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 宏](mci-macros.md)
</dt> </dl>

 

 





