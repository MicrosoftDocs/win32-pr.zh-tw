---
title: IDL 檔案的剖析
description: 這些範例 IDL 檔案示範介面定義的基礎結構。
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531d46bfcfa0ef4e4eee075ae65b64dd0c80a8f6a51543a1762a0ddcd8a03888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311332"
---
# <a name="anatomy-of-an-idl-file"></a>IDL 檔案的剖析

這些範例 IDL 檔案示範介面定義的基礎結構。 記憶體配置、自訂封送處理和非同步訊息只是您可以在自訂 COM 介面中執行的幾項功能。 MIDL 屬性是用來定義 COM 介面。 如需有關如何執行介面和型別程式庫的詳細資訊，包括 MIDL 屬性的摘要，請參閱 MIDL 程式設計師指南和參考中的 [介面定義和型別程式庫](/windows/desktop/Midl/interface-definitions-and-type-libraries) 。 如需所有 MIDL 屬性、關鍵字和指示詞的完整參考，請參閱 [MIDL 語言參考](/windows/desktop/Midl/midl-language-reference)。

## <a name="exampleidl"></a>範例 .idl

下列範例 IDL 檔案會定義兩個 COM 介面。 從這個 IDL 檔案，Midl.exe 將會產生 proxy/stub，以及封送處理常式代碼和標頭檔。 剖析會遵循範例。

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

在這裡使用 IDL 匯 [**入**](/windows/desktop/Midl/import) 語句來帶入標頭檔（Mydefs），其中包含使用者定義型別，以及 Unknwn 包含 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)的定義，其中 IFace1 和 IFace2 衍生自後者。

[**Object**](/windows/desktop/Midl/object)屬性將介面識別為物件介面，並告知 MIDL 編譯器產生 proxy/stub 程式碼，而不是 RPC 用戶端和伺服器 stub。 物件介面方法的傳回類型必須是 [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)，以允許基礎 RPC 機制回報因網路問題而無法完成的呼叫錯誤。

[**Uuid**](/windows/desktop/Midl/uuid)屬性會指定 (IID) 的介面識別碼。 每個介面、類別和類型程式庫都必須使用自己的唯一識別碼來識別。 使用公用程式 Uuidgen.exe 為您的介面和其他元件產生一組唯一的識別碼。

[**Interface**](/windows/desktop/Midl/interface)關鍵字會定義介面名稱。 所有物件介面都必須直接或間接衍生自 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)。

[**In**](/windows/desktop/Midl/in)方向參數指定僅由呼叫端設定的參數。 [**Out**](/windows/desktop/Midl/out-idl)參數會指定傳回給呼叫端的資料。 在一個參數上使用這兩個方向屬性，可指定使用參數將資料傳送至方法，並將資料傳回給呼叫端。

[**指標 \_ default**](/windows/desktop/Midl/pointer-default)屬性指定預設指標類型 (除了參數清單中包含的所有指標以外的 [**唯一**](/windows/desktop/Midl/unique)、 [**ref**](/windows/desktop/Midl/ref)或 [**ptr**](/windows/desktop/Midl/ptr)) 。 如果未指定預設型別，MIDL 會假設單一指標是 **唯一** 的。 但是，當您有多個層級的指標時，您必須明確指定預設的指標類型，即使您想要讓預設型別成為 **唯一** 的。

在上述範例中，陣列 BkfstStuff \[ \] 是 *符合標準的陣列*，這是在執行時間決定的大小。 [**Max \_ 為**](/windows/desktop/Midl/max-is)attribute 指定包含陣列索引最大值的變數。

[**Size \_ 為**](/windows/desktop/Midl/size-is)attribute 也用來指定陣列的大小，或（如同上述範例中的多個指標層級）。 在此範例中，您可以在不事先知道將傳回多少資料的情況下進行呼叫。

## <a name="example2idl"></a>Example2 .idl

下列 IDL 範例 (會重複使用先前 IDL 範例中所述的介面) 顯示產生介面類別型庫資訊的各種方法。

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

[**Helpstring**](/windows/desktop/Midl/helpstring)屬性是選擇性的;您可以使用它來簡短描述物件或提供狀態行。 這些說明字串可使用物件瀏覽器來讀取，例如 Microsoft Visual Basic 所提供的物件瀏覽器。

IFace3 上的 [**雙重**](/windows/desktop/Midl/dual) 屬性會建立同時為分派介面和 COM 介面的介面。 因為它衍生自 **IDispatch**，所以雙重介面支援 Automation，也就是 [**oleautomation**](/windows/desktop/Midl/oleautomation) 屬性所指定的。 IFace3 會匯入 Oaidl.idl，以取得 **IDispatch** 的定義。

[**Library**](/windows/desktop/Midl/library)語句會定義 ExampleLib 類型程式庫，其具有自己的 [**uuid**](/windows/desktop/Midl/uuid)、 [**helpstring**](/windows/desktop/Midl/helpstring)和 [**version**](/windows/desktop/Midl/version)屬性。

在類型程式庫定義內， [**importlib**](/windows/desktop/Midl/importlib) 指示詞會帶入已編譯的類型程式庫。 所有類型程式庫定義都應該帶入 Stdole32 中定義的基底類型程式庫。

此類型程式庫定義示範三種不同的方式，可將介面包含在類型程式庫中。 IFace3 只會在程式庫語句內進行參考而包含在內。

[**Coclass**](/windows/desktop/Midl/coclass)語句會定義全新的元件類別 BkfstComponent，其中包含兩個先前定義的介面 IFace1 和 IFace2。 預設屬性會將 IFace1 指定為預設介面。

IFace4 描述于 library 語句內。 MethodD 上的 [**propput**](/windows/desktop/Midl/propput) 屬性工作表示方法會在相同名稱的屬性上執行設定動作。 [**Propget**](/windows/desktop/Midl/propget)屬性指出方法會從與方法相同名稱的屬性中抓取資訊。 MethodD 中的 [**retval**](/windows/desktop/Midl/retval) 屬性指定輸出參數，其中包含函式的傳回值。

 

 
