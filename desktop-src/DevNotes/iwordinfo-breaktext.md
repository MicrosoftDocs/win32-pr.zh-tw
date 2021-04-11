---
description: 剖析文字以識別單字，並將結果提供給 WordSink 物件。
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: IWordInfo：： BreakText 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: f6f71e92137490d56c93d9443506c2d7ffa2688a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025835"
---
# <a name="iwordinfobreaktext-method"></a>IWordInfo：： BreakText 方法

\[此方法已淘汰，且在 Windows Vista 上不受支援。\]

剖析文字以識別單字，並將結果提供給 [WordSink](/previous-versions//ms691570(v=vs.85)) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT BreakText(
  [in] TEXT_SOURCE *pTextSource,
  [in] IWordSink   *pWordSink,
  [in] DWORD       fBreakMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTextSource* \[在\]
</dt> <dd>

[文字 \_ 來源](/previous-versions//ms690919(v=vs.85))結構的指標，其中包含 Unicode 文字。

</dd> <dt>

*pWordSink* \[在\]
</dt> <dd>

[WordSink](/previous-versions//ms691570(v=vs.85))物件的指標，該物件會接收並處理這個方法所產生的單字。 如果此參數為 **Null**，則此方法不會將字串分成單字。

</dd> <dt>

*fBreakMode* \[在\]
</dt> <dd>

中斷模式。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                   | 意義                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_BREAKTEXTMODE \_ DICTFORM**</dt> <dt>0x00000002</dt> </dl> | 將文字字串斷詞，並將字典形式的單字傳遞給 **WordSink** 物件。<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_BREAKTEXTMODE \_ SMARTSEL**</dt> <dt>0x00000001</dt> </dl> | 將文字字串斷詞，並將文字傳遞至 **WordSink** 物件。<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。



| 傳回碼                                                                            | Description                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 作業成功。 沒有其他可用來重填 *pTextSource* 緩衝區的文字。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | *PTextSource* 參數為 **Null**。<br/>                                                     |



 

## <a name="remarks"></a>備註

使用 **文字 \_ 來源** 結構的 **pfnFillTextBuffer** 成員來補充來源文字。 這個方法必須處理來自 **pfnFillTextBuffer** 回呼函式的所有傳回值。 如果發生錯誤，請在處理錯誤之前完成緩衝區中的文字處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[文字 \_ 來源](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
