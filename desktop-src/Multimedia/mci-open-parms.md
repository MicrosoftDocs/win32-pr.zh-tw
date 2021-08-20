---
title: 'MCI_OPEN_PARMS 結構 (Mciapi .h) '
description: MCI \_ open \_ PARMS 結構包含 mci open 命令的資訊 \_ 。
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80d01f41db904cea583f83aa446e718d1067e99e4d8bac3a3c6791ef5696f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138303"
---
# <a name="mci_open_parms-structure"></a>MCI \_ 開啟 \_ PARMS 結構

**Mci \_ open \_ PARMS** 結構包含 [**mci \_ open**](mci-open.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
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

裝置元素通常 (路徑) 。

</dd> <dt>

**lpstrAlias**
</dt> <dd>

選用裝置別名。

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

[**開啟的 MCI \_**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

