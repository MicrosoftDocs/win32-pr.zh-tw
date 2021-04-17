---
description: 介紹使用 Windows Vista SDK 的 Tablet PC 技術章節的 COM 程式庫和注意事項。
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: 使用 COM 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318288"
---
# <a name="using-the-com-library"></a><span data-ttu-id="9eca8-103">使用 COM 程式庫</span><span class="sxs-lookup"><span data-stu-id="9eca8-103">Using the COM Library</span></span>

<span data-ttu-id="9eca8-104">Tablet PC 受控程式庫參考現在可在一般的 Windows Vista SDK 類別庫參考區段中找到。</span><span class="sxs-lookup"><span data-stu-id="9eca8-104">The Tablet PC managed library reference can now be found in the regular Windows Vista SDK Class Library reference section.</span></span> <span data-ttu-id="9eca8-105">它會提供 Microsoft Visual C++ 的物件模型。</span><span class="sxs-lookup"><span data-stu-id="9eca8-105">It provides an object model for Microsoft Visual C++.</span></span> <span data-ttu-id="9eca8-106">COM 程式庫中大部分的物件都與在 Tablet PC 受控 API 中找到的物件完全相同。</span><span class="sxs-lookup"><span data-stu-id="9eca8-106">The majority of the objects in the COM Library are identical to those found in the Tablet PC Managed API.</span></span>

<span data-ttu-id="9eca8-107">不過，除了標準 Microsoft Win32 環境和 Microsoft .NET Frameworksoftware 開發工具組 (SDK) 環境之間的差異之外，COM API 還包含一些成員，這些成員是在受控 API 中找到的成員。</span><span class="sxs-lookup"><span data-stu-id="9eca8-107">However, the COM API contains some members in addition to those found in the Managed API because of differences between the standard Microsoft Win32 environment and the Microsoft .NET Frameworksoftware development kit (SDK) environment.</span></span> <span data-ttu-id="9eca8-108">例如，InkRectangle 和 InkTransform 物件是用於 COM 中，但 FrameworkSDK 提供 [**InkRectangle 類別**](inkrectangle-class.md) 和 [**InkTransform 類別**](inktransform-class.md) 的原生實作為，在 Tablet PC 平臺管理的 API 中不需要這些物件。</span><span class="sxs-lookup"><span data-stu-id="9eca8-108">For example, the InkRectangle and InkTransform objects are used in COM, but the FrameworkSDK provides native implementation for [**InkRectangle Class**](inkrectangle-class.md) and [**InkTransform Class**](inktransform-class.md) that eliminates the need for these objects in the Tablet PC platform Managed API.</span></span>

> [!Note]  
> <span data-ttu-id="9eca8-109">COM API 和筆墨控制項中的物件不是設計用來 (ASP) 的 Active Server 網頁。</span><span class="sxs-lookup"><span data-stu-id="9eca8-109">The objects in the COM API and the ink controls are not designed for use in Active Server Pages (ASP).</span></span>

 

## <a name="working-with-collections"></a><span data-ttu-id="9eca8-110">使用集合</span><span class="sxs-lookup"><span data-stu-id="9eca8-110">Working with Collections</span></span>

<span data-ttu-id="9eca8-111">如果您傳遞 **Null** 值作為 COM 程式庫中任何集合物件的索引，您會收到集合中的第一個專案，因為在進行呼叫時，這些引數值會強制轉型為0。</span><span class="sxs-lookup"><span data-stu-id="9eca8-111">If you pass in a **NULL** value as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

<span data-ttu-id="9eca8-112">**\_ NewEnum** 屬性在介面定義語言中標記為受限制， (集合介面的 IDL) 定義中。</span><span class="sxs-lookup"><span data-stu-id="9eca8-112">The **\_NewEnum** property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.</span></span>

<span data-ttu-id="9eca8-113">在 c + + 中，請 `For...` 先取得集合的長度，以使用迴圈逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="9eca8-113">In C++, use a `For...` loop to iterate through a collection by first obtaining the collection's length.</span></span> <span data-ttu-id="9eca8-114">下列範例顯示如何逐一查看 [**InkDisp**](inkdisp-class.md) 物件的筆劃 `pInk` 。</span><span class="sxs-lookup"><span data-stu-id="9eca8-114">The example below shows how to iterate through the strokes of an [**InkDisp**](inkdisp-class.md) object, `pInk`.</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9eca8-115">參數</span><span class="sxs-lookup"><span data-stu-id="9eca8-115">Parameters</span></span>

<span data-ttu-id="9eca8-116">如果您以 VT \_ 空白或 vt \_ Null 做為 COM 程式庫中任何集合物件的索引，您會收到集合中的第一個專案，因為在進行呼叫時，這些引數值會強制轉型為0。</span><span class="sxs-lookup"><span data-stu-id="9eca8-116">If you pass in VT\_EMPTY or VT\_NULL as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

## <a name="using-idispatch"></a><span data-ttu-id="9eca8-117">使用 IDispatch</span><span class="sxs-lookup"><span data-stu-id="9eca8-117">Using IDispatch</span></span>

<span data-ttu-id="9eca8-118">為了提高效能，Tablet PC Platform COM 應用程式開發介面 (API) 不支援使用 `IDispatchImpl::Invoke` 具有具名引數的 DISPPARAMS 結構來呼叫。</span><span class="sxs-lookup"><span data-stu-id="9eca8-118">To increase performance, the Tablet PC Platform COM application programming interface (API) does not support calling `IDispatchImpl::Invoke` with a DISPPARAMS structure with named arguments.</span></span> <span data-ttu-id="9eca8-119">`IDispatchImpl::GetIDsOfNames`也不支援。</span><span class="sxs-lookup"><span data-stu-id="9eca8-119">The `IDispatchImpl::GetIDsOfNames` is also not supported.</span></span> <span data-ttu-id="9eca8-120">相反地，請 `Invoke` 使用 SDK 標頭中提供的 dispid 來呼叫。</span><span class="sxs-lookup"><span data-stu-id="9eca8-120">Instead, call `Invoke` with the DISPIDs supplied in the SDK headers.</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="9eca8-121">等候事件</span><span class="sxs-lookup"><span data-stu-id="9eca8-121">Waiting for Events</span></span>

<span data-ttu-id="9eca8-122">Tablet PC 環境為多執行緒。</span><span class="sxs-lookup"><span data-stu-id="9eca8-122">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="9eca8-123">請參閱 COM 檔以進行多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="9eca8-123">Refer to COM documentation for multi-threading.</span></span>

## <a name="support-for-aggregation"></a><span data-ttu-id="9eca8-124">支援匯總</span><span class="sxs-lookup"><span data-stu-id="9eca8-124">Support for Aggregation</span></span>

<span data-ttu-id="9eca8-125">只有 [InkEdit](inkedit-control-reference.md) 控制項、 [InkPicture](inkpicture-control-reference.md) 控制項、 [**InkDisp**](inkdisp-class.md) 物件和 [**InkOverlay**](inkoverlay-class.md) 物件已測試過匯總。</span><span class="sxs-lookup"><span data-stu-id="9eca8-125">Aggregation has been tested for only the [InkEdit](inkedit-control-reference.md) control, the [InkPicture](inkpicture-control-reference.md) control, the [**InkDisp**](inkdisp-class.md) object, and the [**InkOverlay**](inkoverlay-class.md) object.</span></span> <span data-ttu-id="9eca8-126">尚未測試程式庫中其他控制項和物件的匯總。</span><span class="sxs-lookup"><span data-stu-id="9eca8-126">Aggregation has not been tested for other controls and objects in the library.</span></span>

## <a name="c"></a><span data-ttu-id="9eca8-127">C++</span><span class="sxs-lookup"><span data-stu-id="9eca8-127">C++</span></span>

<span data-ttu-id="9eca8-128">在 c + + 中使用 Tablet PC SDK 需要使用某些 COM 概念，例如 VARIANT、SAFEARRAY 和 BSTR。</span><span class="sxs-lookup"><span data-stu-id="9eca8-128">Using the Tablet PC SDK in C++ requires the use of some COM concepts, such as VARIANT, SAFEARRAY, and BSTR.</span></span> <span data-ttu-id="9eca8-129">本節說明如何使用它們。</span><span class="sxs-lookup"><span data-stu-id="9eca8-129">This section describes how to use them.</span></span>

### <a name="variant-and-safearray"></a><span data-ttu-id="9eca8-130">VARIANT 和 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="9eca8-130">VARIANT and SAFEARRAY</span></span>

<span data-ttu-id="9eca8-131">VARIANT 結構用於 COM 物件之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="9eca8-131">The VARIANT structure is used for communication between COM objects.</span></span> <span data-ttu-id="9eca8-132">基本上，VARIANT 結構是大型聯集的容器，它會攜帶許多類型的資料。</span><span class="sxs-lookup"><span data-stu-id="9eca8-132">Essentially, the VARIANT structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="9eca8-133">結構中第一個成員的值（vt）描述了哪些 union 成員是有效的。</span><span class="sxs-lookup"><span data-stu-id="9eca8-133">The value in the first member of the structure, vt, describes which of the union members is valid.</span></span> <span data-ttu-id="9eca8-134">當您在 VARIANT 結構中接收資訊時，請檢查 vt 成員以找出哪些成員包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="9eca8-134">When you receive information in a VARIANT structure, check the vt member to find out which member contains valid data.</span></span> <span data-ttu-id="9eca8-135">同樣地，當您使用 VARIANT 結構傳送資訊時，請一律設定 vt 以反映包含資訊的聯集成員。</span><span class="sxs-lookup"><span data-stu-id="9eca8-135">Similarly, when you send information using a VARIANT structure, always set vt to reflect the union member that contains the information.</span></span>

<span data-ttu-id="9eca8-136">使用結構之前，請呼叫 VariantInit COM 函式將它初始化。</span><span class="sxs-lookup"><span data-stu-id="9eca8-136">Before using the structure, initialize it by calling the VariantInit COM function.</span></span> <span data-ttu-id="9eca8-137">完成結構之後，請先將它清除，然後再呼叫 VariantClear 來釋放包含 VARIANT 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9eca8-137">When finished with the structure, clear it before the memory that contains the VARIANT is freed by calling VariantClear.</span></span>

<span data-ttu-id="9eca8-138">如需 VARIANT 結構的詳細資訊，請參閱 [variant 和 VARIANTARG 資料類型](/windows/win32/api/oaidl/ns-oaidl-variant)。</span><span class="sxs-lookup"><span data-stu-id="9eca8-138">For more information on the VARIANT structure, see [VARIANT and VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="9eca8-139">SAFEARRAY 結構是提供來安全地在 COM 中使用陣列的方法。</span><span class="sxs-lookup"><span data-stu-id="9eca8-139">The SAFEARRAY structure is provided as a way to safely work with arrays in COM.</span></span> <span data-ttu-id="9eca8-140">VARIANT 的 parray 欄位是指向 SAFEARRAY 的指標。</span><span class="sxs-lookup"><span data-stu-id="9eca8-140">The VARIANT's parray field is a pointer to a SAFEARRAY.</span></span> <span data-ttu-id="9eca8-141">使用 SafeArrayCreateVector、SafeArrayAccessData 和 SafeArrayUnaccessData 之類的函式，在 VARIANT 中建立並填入 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="9eca8-141">Use functions such as SafeArrayCreateVector, SafeArrayAccessData, and SafeArrayUnaccessData to create and fill a SAFEARRAY in a VARIANT.</span></span>

<span data-ttu-id="9eca8-142">如需 SAFEARRAY 資料類型的詳細資訊，請參閱 [Safearray 資料類型](/windows/win32/api/oaidl/ns-oaidl-safearray)。</span><span class="sxs-lookup"><span data-stu-id="9eca8-142">For more information on the SAFEARRAY data type, see [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

<span data-ttu-id="9eca8-143">這個 c + + 範例 [](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)會 `pInkStrokeDisp` 從 point 資料的陣列建立 IInkStrokeDisp，在 [**InkDisp**](inkdisp-class.md)物件中 `pInk` 。</span><span class="sxs-lookup"><span data-stu-id="9eca8-143">This C++ example creates an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp`, in an [**InkDisp**](inkdisp-class.md) object, `pInk`, from an array of point data.</span></span>


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



### <a name="bstr"></a><span data-ttu-id="9eca8-144">BSTR</span><span class="sxs-lookup"><span data-stu-id="9eca8-144">BSTR</span></span>

<span data-ttu-id="9eca8-145">支援的 COM 字串格式為 BSTR。</span><span class="sxs-lookup"><span data-stu-id="9eca8-145">The supported string format for COM is BSTR.</span></span> <span data-ttu-id="9eca8-146">BSTR 擁有以零結尾的字串指標，但它也包含字串 (的長度（以位元組為單位），而不是計算結束字元) ，其儲存在字串的第一個字元之前的4個位元組中。</span><span class="sxs-lookup"><span data-stu-id="9eca8-146">A BSTR has a pointer to a zero-terminated string, but it also contains the length of the string (in bytes, not counting the terminator), which is stored in the 4 bytes immediately preceding the first character of the string.</span></span>

<span data-ttu-id="9eca8-147">如需 BSTR 的詳細資訊，請參閱 [Bstr 資料類型](/previous-versions/windows/desktop/automat/bstr)。</span><span class="sxs-lookup"><span data-stu-id="9eca8-147">For more information on BSTR, see [BSTR Data Type](/previous-versions/windows/desktop/automat/bstr).</span></span>

<span data-ttu-id="9eca8-148">這個 c + + 範例示範如何使用 BSTR 來設定 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 上的模擬。</span><span class="sxs-lookup"><span data-stu-id="9eca8-148">This C++ sample shows how to set the factoid on an [**InkRecognizerContext**](inkrecognizercontext-class.md) using a BSTR.</span></span>


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



 

 
