---
description: AttachByReader 方法會在指定的讀取器中開啟智慧卡。
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'ISCard：： AttachByReader 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945036"
---
# <a name="iscardattachbyreader-method"></a>ISCard：： AttachByReader 方法

\[**AttachByReader** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**AttachByReader** 方法會在指定的 [*讀取器*](../secgloss/r-gly.md)中開啟 [*智慧卡*](../secgloss/s-gly.md)。

## <a name="syntax"></a>語法


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrReaderName* \[在\]
</dt> <dd>

包含智慧卡讀卡機名稱的 **BSTR** 。

</dd> <dt>

*ShareMode* \[在\]
</dt> <dd>

要在其中索取智慧卡存取權的模式。



| 值                                                                                                                                            | 意義                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**獨家**</dt> </dl> | 沒有其他人使用此智慧卡連線。<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**共用**</dt> </dl>          | 其他應用程式可以使用此連接。<br/>        |



 

</dd> <dt>

*PrefProtocol* \[在\]
</dt> <dd>

慣用的通訊協定值。

<dl><span id="T0"></span><span id="t0"></span><dt>

**T0**
</dt><span id="T1"></span><span id="t1"></span><dt>

**T1**
</dt><span id="RAW"></span><span id="raw"></span><dt>

**RAW**
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

**T0 \| T1**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | Description                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 在名為讀取器的智慧卡上開啟，已順利完成。<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 傳遞至函式的一或多個參數發生問題。<br/> |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

當您完成使用讀取器時，請呼叫 [**ISCard：:D etach**](iscard-detach.md) 方法來釋放附件。

## <a name="examples"></a>範例

下列範例顯示如何在指定的智慧卡讀卡機中附加至智慧卡。


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardmgr。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardmgr .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**中斷連結**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**附加**](iscard-reattach.md)
</dt> </dl>

 

 
