---
title: 基本和自訂系結控制碼
description: 以控制碼 t 或 RPC 系結控制碼類型宣告的所有控制碼 \_ \_ \_ 都是基本的系結控制碼。
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0e1d6f7cc2ad4d11e268e0f5c83b0275fcd2677a32303820507272f550b834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019148"
---
# <a name="primitive-and-custom-binding-handles"></a>基本和自訂系結控制碼

以 [控制碼 \_ t](/windows/desktop/Midl/handle-t) 或 RPC 系結 [**\_ \_ 控制碼**](rpc-binding-handle.md) 類型宣告的所有控制碼都是基本的系結控制碼。 您可以擴充 [控制碼 \_ t](/windows/desktop/Midl/handle-t) 或 [**RPC 系結 \_ \_ 控制碼**](rpc-binding-handle.md) 類型，以包含更多或不同于基本控制碼類型所包含的資訊。 當您這樣做時，您會建立自訂系結控制碼。

若要為您的分散式應用程式建立自訂系結控制碼，您必須建立自己的資料類型，並在 IDL 檔案的 \[ 類型定義上指定[控制碼](/windows/desktop/Midl/handle) \] 屬性。 最後，存根檔案會將自訂系結控制碼對應至基本控制碼。

如果您建立自己的系結控制碼類型，您也必須提供系結和解除系結程式，用戶端 stub 會使用這些常式將自訂控制碼對應至基本控制碼。 Stub 會在每個遠端程序呼叫的開頭和結尾呼叫您的系結和解除系結常式。 系結和解除系結常式必須符合下列函式原型。



| 函式原型                     | 描述       |
|----------------------------------------|-------------------|
| 處理 \_ t 類型系結 \_ (*類型*)            | 系結常式   |
| void 類型 \_ 解除系結 (*類型*， *處理 \_ t*)  | 解除系結常式 |



 

下列範例顯示如何在 IDL 檔案中定義自訂系結控制碼：

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

如果系結常式遇到錯誤，則應該使用 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 函數引發例外狀況。 然後，用戶端 stub 將會清除，讓例外狀況篩選至用戶端上遠端程序呼叫周圍的例外狀況區塊。 如果系結常式只會傳回 **Null**，用戶端程式代碼會取得錯誤 RPC S 不正確系結 \_ \_ \_ 。 雖然在某些情況下這可能是可接受的，但在其他情況下 (例如記憶體不足) 也不會有任何回應。 解除系結常式應設計為不會失敗。 解除系結常式不應引發例外狀況。

程式設計師定義的系結和解除系結常式會出現在用戶端應用程式中。 在下列範例中，bind 常式會呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) ，以將字串系結資訊轉換成系結控制碼。 解除系結常式會呼叫 [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) ，以釋放系結控制碼。

程式設計師定義的系結控制碼名稱（資料 \_ 控制碼 \_ 類型）會顯示為函式名稱的一部分。 它也會當做函數參數中的參數類型使用。

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

隱含和明確的系結控制碼可以是基本或自訂控制碼。 也就是說，控制碼可以是：

-   基本和隱含
-   自訂和隱含
-   基本和明確
-   自訂和明確

 

 