---
title: 回呼屬性
description: '\ 回呼 \ 屬性會宣告存在於分散式應用程式的用戶端上的靜態回呼函數。 回呼函數可讓伺服器在用戶端上執行程式碼。'
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- 回呼屬性 MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77eb93a78553ccbc95b1671dc215012eeccc56b0bff8ea23e47f68aaf51e10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807334"
---
# <a name="callback-attribute"></a>回呼屬性

**\[ 回呼 \]** 屬性會宣告存在於分散式應用程式之用戶端的靜態回呼函數。 回呼函數可讓伺服器在用戶端上執行程式碼。

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*函數-attr-list* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md)和 **\]** **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。 以逗號分隔多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底 \_ 類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*ptr 宣告子* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定適用于指定之參數類型的零或多個方向屬性、欄位屬性、使用方式屬性和指標屬性。 以逗號分隔多個屬性。

</dd> <dt>

*符中* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 參數名稱識別碼是選擇性的。

</dd> </dl>

## <a name="remarks"></a>備註

當伺服器必須從用戶端取得資訊時， **\[ 回檔 \]** 函式很有用。 如果 Windows 3 支援伺服器應用程式。*x*，伺服器可以對 Windows 3 的遠端程式進行呼叫。*x* 伺服器以取得所需的資訊。 回呼函式會完成相同的目的，並讓伺服器查詢用戶端以取得原始呼叫內容中的資訊。

回呼是在單一線程中執行之遠端呼叫的特殊案例。 回呼是在遠端呼叫的內容中發出。 任何定義為與靜態回呼函式相同之介面一部分的遠端程式，都可以呼叫回呼函式。

請務必注意， \[ \] 不建議在多執行緒程式設計中使用回呼。 作為單一執行緒程式設計功能，它並不支援多執行緒環境所提供的安全性需求。

**RpcCancelThread** 函數無法用來取消可能分派靜態回呼的呼叫。 如果特定遠端程序呼叫不會產生回呼，則可以取消。 否則，只有在可以保證呼叫的回呼尚未發出時，才能取消呼叫。

只有連接導向和本機通訊協定序列支援回呼屬性。 \[ \] 本機通訊協定序列的回呼資料大小限制為150個位元組。 如果 RPC 介面使用不需連線的 (資料包) 通訊協定順序，則對回呼屬性之程式的呼叫將會失敗。

控制碼不能當做回呼函數中的參數使用。 由於回呼一律是在呼叫的內容中執行，因此用戶端用來對伺服器進行呼叫的系結控制碼也會當做伺服器對用戶端的系結控制碼使用。

回呼可以嵌套到任何深度。

## <a name="examples"></a>範例

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 