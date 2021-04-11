---
title: '預先定義的區間 (Ctffunc .h) '
description: 下列值會識別文字服務架構所執行的區間。
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- 預先定義的區間文字服務架構
topic_type:
- apiref
api_name:
- Predefined Compartments
api_location:
- Ctffunc.h
- Mstctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc684c4aee55c3c2e1807458ee261ad55156e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105390"
---
# <a name="predefined-compartments"></a>預先定義的區間

下列值會識別文字服務架構所執行的區間。

下列區間識別碼定義于 Ctffunc .idl 和 Ctffunc 中。



| 旗標                                     | 值  | 描述                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID 區間的 \_ \_ SAPI \_ 音訊           | VT \_ I4 | 如果語音 API (SAPI) 音訊為零，則為 **零，如果** sapi 音訊為開啟，則為非零。 這個區間是執行緒管理員物件專用的。                                                                                                                               |
| GUID \_ 區間 \_ 語音 \_ CFGMENU       | VT \_ I4 | 如果 [語音設定] 功能表無法使用，則為零，如果 [語音設定] 功能表可用則為非零的 **DWORD** 。 這個區間是執行緒管理員物件專用的。                                                                                               |
| GUID \_ 區間 \_ 語音 \_ DICTATIONSTAT | VT \_ I4 | **DWORD** 值，包含一或多個 [**\_ \_ 已啟用的 tf 聽寫**](speech-recognition-constants.md)、 **\_ \_ 已啟用 tf 命令**、 **\_ \_ on** 或 **tf \_ 命令 \_ on** 值的組合。 這個區間是執行緒管理員物件專用的。 |
| GUID \_ 區間 \_ 語音 \_ UI \_ 狀態    | VT \_ I4 | **DWORD** 值，包含一或多個 [**TF \_ SHOW \_ balloon**](speech-recognition-constants.md)或 **tf \_ 停用 \_ 氣球** 值的零或組合。 這是全域區間。                                                                                   |



 

下列區間識別碼定義于 MSCTF 中。IDL 和 MSCTF .H。



| 旗標                                                    | 值  | 描述                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ 區間 \_ EMPTYCONTEXT                         | VT \_ I4 | 如果內容是空的，則為非零的 **DWORD** ，否則為零。 此區間為內容物件所特有。                                                                                                                                      |
| GUID \_ 區間 \_ 手寫 \_ OPENCLOSE               | VT \_ I4 | **DWORD** ，如果手寫辨識為開啟，則為非零，如果手寫辨識已關閉，則為零。 這個區間是執行緒管理員物件專用的。                                                                                 |
| GUID \_ 區間 \_ 鍵盤 \_ 已停用                   | VT \_ I4 | 如果鍵盤已停用，則為非零的 **DWORD** ，否則為零。 此區間為內容物件所特有。                                                                                                                                  |
| GUID \_ 區間 \_ 鍵盤 \_ INPUTMODE \_ 轉換      | VT \_ I4 | [**TF \_ CONVERSIONMODE \_**](flags-for-conversion-mode.md)旗標適當組合的 **DWORD** 值。 這個區間是執行緒管理員物件專用的。                                                                                      |
| GUID \_ 區間 \_ 鍵盤 \_ INPUTMODE \_ 句子        | VT \_ I4 | [**TF \_ SENTENCEMODE \_**](flags-for-conversion-mode.md)的 **DWORD** 值。 這個區間是執行緒管理員物件專用的。                                                                                                                        |
| GUID \_ 區間 \_ 鍵盤 \_ OPENCLOSE                  | VT \_ I4 | 如果鍵盤已開啟則為非零的 **DWORD** ，如果鍵盤已關閉，則為零。 這個區間是執行緒管理員物件專用的。                                                                                                               |
| GUID \_ 區間 \_ PERSISTMENUENABLED                   | VT \_ I4 | **DWORD** ，非零值，讓語音文字服務啟用 [**儲存語音資料**] 功能表項目，或使用零來停用它。 這個區間是檔案管理員物件特有的。                                                                   |
| GUID \_ 區間 \_ 語音 \_ 已停用                     | VT \_ I4 | **DWORD** ，其中包含一或多個 [**TF \_ disable \_ SPEECH**](speech-recognition-constants.md)、 **tf \_ disable \_ 聽寫** 或 **TF \_ 停用 \_ 命令** 值的零或組合。 這個區間是執行緒管理員物件專用的。 |
| GUID \_ 區間 \_ 語音 \_ OPENCLOSE                    | VT \_ I4 | 如果語音輸入為使用中，則為非零的 **DWORD** ，如果語音輸入為非使用中，則為零。 這是全域區間。                                                                                                                                      |
| GUID \_ 區間 \_ TIPUISTATUS                          | VT \_ I4 | 目前無法使用。                                                                                                                                                                                                                                           |
| GUID \_ 區間 \_ TRANSITORYEXTENSION                  | VT \_ I4 | [**Tf \_ TRANSITORYEXTENSION \_ NONE**](values-for-guid-compartment-transitoryextension.md)、 **tf \_ TRANSITORYEXTENSION \_ 浮動** 或 **tf \_ TRANSITORYEXTENSION \_ ATSELECTION** 的 **DWORD** 值。 這個區間是檔案管理員物件特有的。  |
| GUID \_ 區間 \_ TRANSITORYEXTENSION \_ DOCUMENTMANAGER | VT \_ I4 | [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)介面的 IUnknown 值，參考此檔管理員的暫時性檔。 這個區間是檔案管理員物件特有的。                                                         |
| GUID \_ 區間 \_ TRANSITORYEXTENSION \_ 父系          | VT \_ I4 | [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)介面的 IUnknown 值，參考此暫時性檔的父檔管理員。 這個區間是檔案管理員物件特有的。                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                                                                                          |
| 標頭<br/>                   | <dl> <dt>Ctffunc .h;</dt><dt>Mstctf .h</dt> </dl>     |
| Idl<br/>                      | <dl> <dt>Ctffunc .idl;</dt><dt>Mstctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**語音辨識常數**](speech-recognition-constants.md)
</dt> </dl>

 

 





