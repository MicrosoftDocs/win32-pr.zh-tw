---
title: 'MCI_WAVE_OPEN_PARMS 結構 (Mciapi .h) '
description: MCI \_ WAVE \_ open PARMS 結構包含適用于 wave \_ 音訊裝置的 mci \_ open 命令資訊。
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- MCI_WAVE_OPEN_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966517"
---
# <a name="mci_wave_open_parms-structure"></a>MCI \_ WAVE \_ 開啟 \_ PARMS 結構

**Mci \_ WAVE \_ open \_ PARMS** 結構包含適用于 wave 音訊裝置的 [**mci \_ open**](mci-open.md)命令資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**wDeviceID**
</dt> <dd>

識別碼傳回至應用程式。

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

裝置類型的名稱或常數識別碼。  (裝置的名稱通常是從登錄或 SYSTEM.INI 檔案取得。 ) 此成員可以是 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。

</dd> <dt>

**lpstrElementName**
</dt> <dd>

裝置元素名稱通常 (路徑) 。

</dd> <dt>

**lpstrAlias**
</dt> <dd>

選用裝置別名。

</dd> <dt>

**dwBufferSeconds**
</dt> <dd>

緩衝區長度（以秒為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

如果您不是使用擴充的資料成員，您可以使用 [**mci \_ open \_ PARMS**](mci-open-parms.md) 結構，而不是 **mci \_ WAVE \_ open \_ PARMS** 。

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

[**開啟的 MCI \_**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCI \_ 開啟 \_ PARMS**](mci-open-parms.md)
</dt> </dl>

 

