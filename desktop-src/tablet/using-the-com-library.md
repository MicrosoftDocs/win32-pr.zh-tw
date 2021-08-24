---
description: 介紹使用 Windows Vista SDK 的 Tablet PC 技術章節的 COM 程式庫和注意事項。
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: 使用 COM 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf986d79011301abe6a9f279a83278fda5dd9e33e3a79335d7d94e6081fb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819138"
---
# <a name="using-the-com-library"></a>使用 COM 程式庫

Tablet PC 受控程式庫參考現在可在一般的 Windows Vista SDK 類別庫參考一節中找到。 它會提供 Microsoft Visual C++ 的物件模型。 COM 程式庫中大部分的物件都與在 Tablet PC 受控 API 中找到的物件完全相同。

不過，除了標準 Microsoft Win32 環境和 Microsoft .NET Frameworksoftware 開發工具組 (SDK) 環境之間的差異之外，COM API 還包含一些成員，這些成員是在受控 API 中找到的成員。 例如，InkRectangle 和 InkTransform 物件是用於 COM 中，但 FrameworkSDK 提供 [**InkRectangle 類別**](inkrectangle-class.md) 和 [**InkTransform 類別**](inktransform-class.md) 的原生實作為，在 Tablet PC 平臺管理的 API 中不需要這些物件。

> [!Note]  
> COM API 和筆墨控制項中的物件不是設計用來 (ASP) 的 Active Server 網頁。

 

## <a name="working-with-collections"></a>使用集合

如果您傳遞 **Null** 值作為 COM 程式庫中任何集合物件的索引，您會收到集合中的第一個專案，因為在進行呼叫時，這些引數值會強制轉型為0。

**\_ NewEnum** 屬性在介面定義語言中標記為受限制， (集合介面的 IDL) 定義中。

在 c + + 中，請 `For...` 先取得集合的長度，以使用迴圈逐一查看集合。 下列範例顯示如何逐一查看 [**InkDisp**](inkdisp-class.md) 物件的筆劃 `pInk` 。


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a>參數

如果您以 VT \_ 空白或 vt \_ Null 做為 COM 程式庫中任何集合物件的索引，您會收到集合中的第一個專案，因為在進行呼叫時，這些引數值會強制轉型為0。

## <a name="using-idispatch"></a>使用 IDispatch

為了提高效能，Tablet PC Platform COM 應用程式開發介面 (API) 不支援使用 `IDispatchImpl::Invoke` 具有具名引數的 DISPPARAMS 結構來呼叫。 `IDispatchImpl::GetIDsOfNames`也不支援。 相反地，請 `Invoke` 使用 SDK 標頭中提供的 dispid 來呼叫。

## <a name="waiting-for-events"></a>等候事件

Tablet PC 環境為多執行緒。 請參閱 COM 檔以進行多執行緒處理。

## <a name="support-for-aggregation"></a>支援匯總

只有 [InkEdit](inkedit-control-reference.md) 控制項、 [InkPicture](inkpicture-control-reference.md) 控制項、 [**InkDisp**](inkdisp-class.md) 物件和 [**InkOverlay**](inkoverlay-class.md) 物件已測試過匯總。 尚未測試程式庫中其他控制項和物件的匯總。

## <a name="c"></a>C++

在 c + + 中使用 Tablet PC SDK 需要使用某些 COM 概念，例如 VARIANT、SAFEARRAY 和 BSTR。 本節說明如何使用它們。

### <a name="variant-and-safearray"></a>VARIANT 和 SAFEARRAY

VARIANT 結構用於 COM 物件之間的通訊。 基本上，VARIANT 結構是大型聯集的容器，它會攜帶許多類型的資料。

結構中第一個成員的值（vt）描述了哪些 union 成員是有效的。 當您在 VARIANT 結構中接收資訊時，請檢查 vt 成員以找出哪些成員包含有效的資料。 同樣地，當您使用 VARIANT 結構傳送資訊時，請一律設定 vt 以反映包含資訊的聯集成員。

使用結構之前，請呼叫 VariantInit COM 函式將它初始化。 完成結構之後，請先將它清除，然後再呼叫 VariantClear 來釋放包含 VARIANT 的記憶體。

如需 VARIANT 結構的詳細資訊，請參閱 [variant 和 VARIANTARG 資料類型](/windows/win32/api/oaidl/ns-oaidl-variant)。

SAFEARRAY 結構是提供來安全地在 COM 中使用陣列的方法。 VARIANT 的 parray 欄位是指向 SAFEARRAY 的指標。 使用 SafeArrayCreateVector、SafeArrayAccessData 和 SafeArrayUnaccessData 之類的函式，在 VARIANT 中建立並填入 SAFEARRAY。

如需 SAFEARRAY 資料類型的詳細資訊，請參閱 [Safearray 資料類型](/windows/win32/api/oaidl/ns-oaidl-safearray)。

這個 c + + 範例 [](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)會 `pInkStrokeDisp` 從 point 資料的陣列建立 IInkStrokeDisp，在 [**InkDisp**](inkdisp-class.md)物件中 `pInk` 。


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a>BSTR

支援的 COM 字串格式為 BSTR。 BSTR 擁有以零結尾的字串指標，但它也包含字串 (的長度（以位元組為單位），而不是計算結束字元) ，其儲存在字串的第一個字元之前的4個位元組中。

如需 BSTR 的詳細資訊，請參閱 [Bstr 資料類型](/previous-versions/windows/desktop/automat/bstr)。

這個 c + + 範例示範如何使用 BSTR 來設定 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 上的模擬。


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
