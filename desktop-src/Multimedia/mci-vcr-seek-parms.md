---
title: 'MCI_VCR_SEEK_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 搜尋 \_ PARMS 結構包含適用于 video 的 mci \_ 搜尋命令的參數。
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464833"
---
# <a name="mci_vcr_seek_parms-structure"></a>MCI \_ VCR \_ 搜尋 \_ PARMS 結構

**Mci \_ VCR \_ 搜尋 \_ PARMS** 結構包含適用于 video 的 [**mci \_ 搜尋**](mci-seek.md)命令的參數。

## <a name="syntax"></a>語法


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwTo**
</dt> <dd>

要搜尋的位置。

</dd> <dt>

**dwMark**
</dt> <dd>

要搜尋的編號標記。

</dd> <dt>

**dwAt**
</dt> <dd>

開始搜尋的時間。

</dd> </dl>

## <a name="remarks"></a>備註

以目前時間格式指定位置。

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vcr</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 搜尋**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

