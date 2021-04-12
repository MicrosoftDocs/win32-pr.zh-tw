---
title: 'MCI_VD_STEP_PARMS 結構 (Mciapi .h) '
description: MCI \_ VD \_ step \_ PARMS 結構包含適用于 \_ videodisc 裝置之 MCI 步驟命令的資訊。
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- MCI_VD_STEP_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508599"
---
# <a name="mci_vd_step_parms-structure"></a>MCI \_ VD \_ 步驟 \_ PARMS 結構

**Mci \_ VD \_ step \_ PARMS** 結構包含適用于 videodisc 裝置 [**之 MCI \_ 步驟**](mci-step.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwFrames**
</dt> <dd>

要逐步執行的畫面格數目。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mciapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 步驟**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

