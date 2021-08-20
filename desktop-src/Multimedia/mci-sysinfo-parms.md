---
title: 'MCI_SYSINFO_PARMS 結構 (Mciapi .h) '
description: MCI \_ SYSINFO \_ PARMS 結構包含 mci SYSINFO 命令的資訊 \_ 。
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d37f4d011997352a95b80dc80b8b9afd28730feeeb0e285a07d68c8c8eed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803128"
---
# <a name="mci_sysinfo_parms-structure"></a>MCI \_ SYSINFO \_ PARMS 結構

**Mci \_ SYSINFO \_ PARMS** 結構包含 [**mci \_ SYSINFO**](mci-sysinfo.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**lpstrReturn**
</dt> <dd>

傳回字串之使用者提供的緩衝區指標。  \_ 使用 MCI SYSINFO QUANTITY 旗標時，也會使用它來傳回 DWORD 值 \_ 。

</dd> <dt>

**dwRetSize**
</dt> <dd>

傳回緩衝區的大小（以位元組為單位）。

</dd> <dt>

**dwNumber**
</dt> <dd>

如果設定了 MCI \_ SYSINFO 開啟旗標，則會指出 mci 裝置表格或開啟的裝置清單中的裝置位置 \_ 。

</dd> <dt>

**wDeviceType**
</dt> <dd>

裝置類型。 此成員可以是 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。

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

[**MCI \_ SYSINFO**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

