---
title: 'MCI_OVLY_OPEN_PARMS 結構 (Mmsystem .h) '
description: MCI \_ OVLY \_ OPEN \_ PARMS 結構包含適用于影片重迭裝置的 mci \_ OPEN 命令資訊。
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464228"
---
# <a name="mci_ovly_open_parms-structure"></a>MCI \_ OVLY \_ 開啟 \_ PARMS 結構

**Mci \_ OVLY \_ OPEN \_ PARMS** 結構包含適用于影片重迭裝置的 [**mci \_ OPEN**](mci-open.md)命令資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**wDeviceID**
</dt> <dd>

傳回給應用程式的識別碼。

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

裝置類型的名稱或常數識別碼。  (裝置的名稱通常是從登錄或 SYSTEM.INI 檔案取得。 ) 如果這個成員是常數，它可以是 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。

</dd> <dt>

**lpstrElementName**
</dt> <dd>

裝置元素名稱通常 (路徑) 。

</dd> <dt>

**lpstrAlias**
</dt> <dd>

選用裝置別名。

</dd> <dt>

**dwStyle**
</dt> <dd>

視窗樣式。

</dd> <dt>

**hWndParent**
</dt> <dd>

父視窗的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

如果您不是使用擴充的資料成員，您可以使用 [**mci \_ open \_ PARMS**](mci-open-parms.md) 結構來取代 **mci \_ OVLY \_ open \_ PARMS** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Mmsystem。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**開啟的 MCI \_**](mci-open.md)
</dt> <dt>

[**MCI \_ 開啟 \_ PARMS**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

