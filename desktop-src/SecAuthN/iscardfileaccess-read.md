---
description: Read 方法會從指定的檔案讀取並傳回指定的資料。
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: ISCardFileAccess：： Read 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: c44839b9916bdee999eb1fb54d689dd51761c35d71bc3ba828171dda62e05c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923197"
---
# <a name="iscardfileaccessread-method"></a>ISCardFileAccess：： Read 方法

\[**Read** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Read** 方法會從指定的檔案讀取並傳回指定的資料。

## <a name="syntax"></a>語法


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFile* \[在\]
</dt> <dd>

要存取的開啟檔案的控制碼。

</dd> <dt>

*lBytesToRead* \[在\]
</dt> <dd>

要讀取的資料長度 () 或讀取 () 輸出的位元組數目。 傳回 Bstr 陣列形式的檔案清單。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

指定是否應使用安全訊息。

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ 安全 \_ 訊息**
</dt> </dl> </dd> <dt>

*ppBuffer* \[擴展\]
</dt> <dd>

包含讀取資料的 [**IByteBuffer**](ibytebuffer.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
