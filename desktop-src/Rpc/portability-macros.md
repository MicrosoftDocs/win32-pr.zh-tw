---
title: '可攜性宏 (Rpc .h) '
description: RPC 工具藉由將產生的存根檔案和標頭檔中的資料類型與函式傳回型別與每個平臺特有的定義產生關聯，以達成模型、呼叫和命名慣例的獨立性。
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- 可攜性宏 RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "103945579"
---
# <a name="portability-macros"></a>可攜性宏

RPC 工具藉由將產生的存根檔案和標頭檔中的資料類型與函式傳回型別與每個平臺特有的定義產生關聯，以達成模型、呼叫和命名慣例的獨立性。 這些巨集定義可確保任何需要指定的資料類型和 **\_ \_ 函數都指定為目前的物件**。

下圖顯示 MIDL 編譯器套用至 RPC 元件之間函式呼叫的巨集定義：

![顯示 MIDL 套用至函式呼叫之巨集定義的圖表。](images/prog-a29.png)

RPC 宏的定義如下。



| 定義    | 描述                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_RPC \_ API  | 適用于存根對使用者應用程式所進行的呼叫。 這兩個函數都在相同的可執行程式中。                                       |
| \_\_目前的 RPC \_  | 適用于指標的標準巨集定義。 此巨集定義應該會顯示為所有使用者提供之函式簽章的一部分。 |
| \_\_RPC \_ 存根 | 套用至從執行時間程式庫對存根進行的呼叫。 這些呼叫可視為私用。                                                 |
| \_\_RPC \_ 使用者 | 適用于執行時間程式庫對使用者應用程式所進行的呼叫。 這些會跨越 DLL 和應用程式之間的界限。                   |
| RPC \_ 專案    | 適用于應用程式或 stub 對執行時間程式庫所做的呼叫。 此巨集定義會套用至所有 RPC 執行時間函式。           |



 

為了正確地連結 Microsoft RPC 執行時間程式庫、存根和支援常式，某些使用者提供的函式也必須在函式定義中包含這些宏。 當您定義與記憶體管理相關聯的函式、使用者定義的系結控制碼和 **傳輸 \_ 為** 屬性時，請使用宏 **\_ \_ rpc \_ API** ，並在定義與內容控制碼相關聯的內容執行常式時使用宏 **\_ \_ rpc \_ 使用者**。 將函數指定為：

<dl> <dt>

<span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC \_ 使用者 *midl \_ 使用者* \_ 配置 ( ... ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC \_ 使用者 *midl \_ 使用者* \_ 可用 ( ... ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC \_ 使用者 *handletype* \_ bind ( ... ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC \_ 使用者 *handletype* \_ 解除系結 ( ... ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC \_ 使用者 *類型* \_ 到 \_ 本機
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_本機的 RPC 使用者 *類型* \_ \_
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_ \_ 要 xmit ( 的 RPC 使用者類型 ... \_ ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_來自 xmit ( 的 RPC 使用者 *類型*... \_ \_ ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC \_ 使用者 *類型* \_ 可用 \_ 本機
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC \_ 使用者 *類型* \_ free \_ inst ( ... ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC \_ 使用者 *類型* \_ free \_ xmit ( ... ) 
</dt> <dd></dd> <dt>

<span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC \_ 使用者內容取消 \_ ( ... ) 
</dt> <dd></dd> </dl>

> [!Note]  
> 這些函數中的所有指標參數都必須使用宏 **\_ \_ RPC \_** 來指定。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Rpc。h</dt> </dl> |



 

 





