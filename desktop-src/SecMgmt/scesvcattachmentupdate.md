---
description: '[安全性設定] 嵌入式管理單元會呼叫 SceSvcAttachmentUpdate 函式，以將設定變更傳遞至安全性資料庫。'
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: SceSvcAttachmentUpdate 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690111"
---
# <a name="scesvcattachmentupdate-callback-function"></a>SceSvcAttachmentUpdate 回呼函式

[安全性設定] 嵌入式管理單元會呼叫 **SceSvcAttachmentUpdate** 函式，以將設定變更傳遞至安全性資料庫。

## <a name="syntax"></a>語法


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSceCbInfo* \[在\]
</dt> <dd>

[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的指標，其中包含 SCE 的回呼控制碼和函式指標。

</dd> <dt>

*ServiceInfo* \[在\]
</dt> <dd>

更新的設定資訊。 這項資訊所使用的資料結構是 [**SCESVC 設定 \_ \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 SCESTATUS \_ SUCCESS。 否則會傳回錯誤碼。 如需有關安全性設定錯誤碼的詳細資訊，請參閱 [附件傳回值](management-return-values.md)。

## <a name="remarks"></a>備註

**SceSvcAttachmentUpdate** 函數必須執行下列動作：

-   呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo >pfQueryInfo) ，從安全性資料庫取出目前的基本設定資訊。
-   呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo->pfQueryInfo) ，以從安全性資料庫 (分析) 資訊最後一組差異。
-   使用提供的服務資訊 (查看 *ServiceInfo*) 來計算新的基本設定。
-   使用提供的服務資訊 (查看 *ServiceInfo*) 和分析，以計算新的差異資訊。
-   呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfSetInfo** 成員所指向的回呼函式 (pSceCbInfo >pfSetInfo) ，以在安全性資料庫中設定新的基底設定。
-   呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfSetInfo** 成員所指向的回呼函式 (pSceCbInfo->pfSetInfo) ，在安全性資料庫中設定新的分析資訊。

如需詳細資訊，請參閱[執行 SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SCESVC \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




