---
description: 設定系統時，安全性設定引擎會呼叫 SceSvcAttachmentConfig 函數。
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: SceSvcAttachmentConfig 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690112"
---
# <a name="scesvcattachmentconfig-callback-function"></a>SceSvcAttachmentConfig 回呼函式

設定系統時，安全性設定引擎會呼叫 **SceSvcAttachmentConfig** 函數。

## <a name="syntax"></a>語法


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSceCbInfo* \[在\]
</dt> <dd>

[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的指標，其中包含資料庫控制碼，以及用來查詢、設定和釋放資訊的回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 SCESTATUS \_ SUCCESS。 否則會傳回錯誤碼。 如需有關安全性設定錯誤碼的詳細資訊，請參閱 [附件傳回值](management-return-values.md)。

## <a name="remarks"></a>備註

在執行此函式時，請使用 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo >pfQueryInfo) 以取得設定資訊。 然後使用傳回的資訊來設定服務。

此函數必須執行下列動作：

-   使用 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式，從安全性設定工具中查詢設定資訊 (pSceCbInfo->pfQueryInfo) 。
-   使用設定資訊來設定服務。

如需詳細資訊，請參閱[執行 SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




