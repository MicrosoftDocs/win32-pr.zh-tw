---
description: 分析系統時，安全性設定引擎會呼叫 SceSvcAttachmentAnalyze 函數。
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: SceSvcAttachmentAnalyze 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9bb84cc6a8492c729926b644a246b8ee8a03e1de4c2eae6e3de1fd88c5ba339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004916"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>SceSvcAttachmentAnalyze 回呼函式

分析系統時，安全性設定引擎會呼叫 **SceSvcAttachmentAnalyze** 函數。

## <a name="syntax"></a>語法


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSceCbInfo* \[在\]
</dt> <dd>

[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的指標，其中包含不透明的資料庫控制碼，以及用來查詢、設定和釋放資訊的回呼函數指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 SCESTATUS \_ SUCCESS。 否則會傳回錯誤碼。 如需有關安全性設定錯誤碼的詳細資訊，請參閱 [附件傳回值](management-return-values.md)。

## <a name="remarks"></a>備註

**SceSvcAttachmentAnalyze** 函數必須執行下列動作：

-   從服務直接查詢設定資訊。
-   呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo->pfQueryInfo) 以從安全性資料庫取出資訊。
-   根據類型和語法計算資訊之間的差異。
-   呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfSetInfo** 成員所指向的回呼函式 (pSceCbInfo->pfSetInfo) ，以不同的抓取服務資訊來更新安全性資料庫。

如需詳細資訊，請參閱 [執行 SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[執行 SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




