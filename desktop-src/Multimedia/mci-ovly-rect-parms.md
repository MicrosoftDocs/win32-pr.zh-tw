---
title: 'MCI_OVLY_RECT_PARMS 結構 (Mciapi .h) '
description: MCI \_ OVLY \_ RECT \_ PARMS 結構包含 MCI PUT 和 mci 的位置資訊，其中包含 \_ \_ 適用于影片重迭裝置的命令。
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfd55b2950f6d4268a9af5ee5bdc7fc9c378c4dbaeaa569406339263a2cf85e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039108"
---
# <a name="mci_ovly_rect_parms-structure"></a>MCI \_ OVLY \_ RECT \_ PARMS 結構

**Mci \_ OVLY \_ RECT \_ PARMS** 結構包含 [**mci \_ PUT**](mci-put.md)和 mci 的位置資訊， [**\_ 其中**](mci-where.md)包含適用于影片重迭裝置的命令。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**鋼筋混凝土**
</dt> <dd>

包含位置資訊的矩形。 除了 Windows 的其他部分，以不同的方式處理在 MCI 中的 [矩形](/previous-versions//ms536136(v=vs.85))結構。在 MCI 中， **.rc** 會包含矩形和 rc 的寬度 **。下方** 包含其高度。

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

[**MCI**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ PUT**](mci-put.md)
</dt> <dt>

[**MCI \_ ，其中**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[矩形](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

