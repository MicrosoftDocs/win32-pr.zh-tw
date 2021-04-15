---
title: ACCELTABLEENTRY 結構
description: 描述個別快速鍵對應表資源中的資料。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- ACCELTABLEENTRY 結構功能表和其他資源
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466885"
---
# <a name="acceltableentry-structure"></a>ACCELTABLEENTRY 結構

描述個別快速鍵對應表資源中的資料。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**fFlags**
</dt> <dd>

類型： **WORD**

</dd> <dd>

描述鍵盤快速鍵特性。 這個成員可以有一個或多個 Winuser 的值。



| 值                                                                                                                                                                                                      | 意義                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>TRUE</dt> </dl>    | 快速鍵是一種 [虛擬金鑰程式碼](/windows/desktop/inputdev/virtual-key-codes)。 如果未指定此旗標，則會假設快速鍵指定 ASCII 字元碼。 <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**FNOINVERT**</dt> <dt>0x02</dt> </dl> | 使用快速鍵時，不會反白顯示功能表列上的功能表項目。 這個屬性已過時，而且只是為了與針對16位 Windows 設計的資源檔回溯相容。<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**FSHIFT**</dt> <dt>0x04</dt> </dl>          | 只有當使用者按下 SHIFT 鍵時，才會啟用此加速器。 此旗標只適用于虛擬機器碼。 <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**FCONTROL**</dt> <dt>0x08</dt> </dl>    | 只有當使用者按下 CTRL 鍵時，才會啟用此加速器。 此旗標只適用于虛擬機器碼。 <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt>**FALT**</dt> <dt>0x10</dt> </dl>                | 只有當使用者按下 ALT 鍵時，才會啟用此加速器。 此旗標只適用于虛擬機器碼。 <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | 專案是快速鍵對應表中的最後一個專案。 <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

類型： **WORD**

</dd> <dd>

識別快速鍵的 ANSI 字元值或虛擬按鍵碼。

</dd> <dt>

**Wid**
</dt> <dd>

類型： **WORD**

</dd> <dd>

鍵盤對應鍵的識別碼。 當使用者按下指定的按鍵時，此值會傳遞給視窗程式。

</dd> <dt>

**padding**
</dt> <dd>

類型： **WORD**

</dd> <dd>

插入的位元組數目，以確保此結構在 **DWORD** 界限上對齊。

</dd> </dl>

## <a name="remarks"></a>備註

資源中的所有快速鍵對應表專案都會重複 **ACCELTABLEENTRY** 結構。 資料表中的最後一個專案會標示值0x0080。

如果您將資源的長度分割為8，您可以計算資料表中的元素數目。 然後，您的應用程式可以隨機存取個別的固定長度專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

