---
description: 抓取智慧卡的 ATR 字串。
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'ISCard：： get_Atr 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979326"
---
# <a name="iscardget_atr-method"></a>ISCard：： get \_ Atr 方法

\[**Get \_ Atr** 方法可用於 [需求] 區段中指定的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ Atr** 方法會抓取 [*智慧卡*](../secgloss/s-gly.md)的 [*Atr 字串*](../secgloss/a-gly.md)。

## <a name="syntax"></a>語法


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAtr* \[擴展\]
</dt> <dd>

以 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 形式的位元組緩衝區指標，會在傳回時包含 ATR 字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PpAtr* 參數無效。<br/>           |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppAtr* 中傳遞了錯誤指標。<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 無法取得滿足要求的記憶體。<br/> |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示從智慧卡取出 ATR 字串。


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
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

[**取得 \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**取得 \_ 內容**](iscard-get-context.md)
</dt> <dt>

[**取得 \_ 通訊協定**](iscard-get-protocol.md)
</dt> <dt>

[**取得 \_ 狀態**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**IByteBuffer：： Read**](ibytebuffer-read.md)
</dt> </dl>

 

 
