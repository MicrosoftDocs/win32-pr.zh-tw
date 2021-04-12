---
title: 叫用動作
description: IUPnPService InvokeAction 方法允許在服務物件上叫用動作。
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7550575281681f3f533db90ef1c1034dbaa085
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376201"
---
# <a name="invoking-actions"></a><span data-ttu-id="10193-103">叫用動作</span><span class="sxs-lookup"><span data-stu-id="10193-103">Invoking Actions</span></span>

<span data-ttu-id="10193-104">[**IUPnPService：： InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction)方法允許在服務物件上叫用動作。</span><span class="sxs-lookup"><span data-stu-id="10193-104">The [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) method allows actions to be invoked on Service objects.</span></span> <span data-ttu-id="10193-105">這個方法有兩個輸入參數：動作的名稱，以及該動作的輸入引數陣列。</span><span class="sxs-lookup"><span data-stu-id="10193-105">This method has two input parameters: the name of an action and an array of input arguments to that action.</span></span> <span data-ttu-id="10193-106">此方法有兩個參數：</span><span class="sxs-lookup"><span data-stu-id="10193-106">The method has two parameters:</span></span>

-   <span data-ttu-id="10193-107">參數一個-輸入/輸出參數：該動作的輸出引數陣列。</span><span class="sxs-lookup"><span data-stu-id="10193-107">Parameter one — an input/output parameter: an array of output arguments for that action.</span></span>
-   <span data-ttu-id="10193-108">參數二-輸出參數：傳回值。</span><span class="sxs-lookup"><span data-stu-id="10193-108">Parameter two — an output parameter: a return value.</span></span>

<span data-ttu-id="10193-109">方法會導致在裝置上叫用動作。</span><span class="sxs-lookup"><span data-stu-id="10193-109">The method causes the action to be invoked on the device.</span></span> <span data-ttu-id="10193-110">如果動作造成裝置的狀態變數變更，裝置會產生事件通知。</span><span class="sxs-lookup"><span data-stu-id="10193-110">The device generates event notifications if the action causes state variables of the device to change.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="10193-111">VBScript 範例</span><span class="sxs-lookup"><span data-stu-id="10193-111">VBScript Example</span></span>

<span data-ttu-id="10193-112">下列 VBScript 程式碼範例會在服務物件上叫用兩個動作。</span><span class="sxs-lookup"><span data-stu-id="10193-112">The following VBScript code example invokes two actions on a Service object.</span></span> <span data-ttu-id="10193-113">第一個動作 *GetTrackInfo* 會接受一個輸入引數，也就是一個曲目編號。</span><span class="sxs-lookup"><span data-stu-id="10193-113">The first action, *GetTrackInfo*, takes one input argument, a track number.</span></span> <span data-ttu-id="10193-114">*GetTrackInfo* 動作會傳回追蹤長度作為傳回值。</span><span class="sxs-lookup"><span data-stu-id="10193-114">The *GetTrackInfo* action returns the track length as the return value.</span></span> <span data-ttu-id="10193-115">此動作也有一個 output 引數，如果方法傳回成功，則會包含軌跡標題。</span><span class="sxs-lookup"><span data-stu-id="10193-115">The action also has one output argument, which contains the track title if the method returns success.</span></span>

<span data-ttu-id="10193-116">叫用 *GetTrackInfo* 動作之後，此範例會叫用不採用任何引數的播放動作。</span><span class="sxs-lookup"><span data-stu-id="10193-116">After invoking the *GetTrackInfo* action, the example invokes the Play action, which takes no arguments.</span></span> <span data-ttu-id="10193-117">不過，因為 [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) 的語法需要輸入和輸出引數的陣列，所以此範例必須建立空的陣列 *emptyArgs*，但不含任何元素。</span><span class="sxs-lookup"><span data-stu-id="10193-117">However, because the syntax of [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires an array of both input and output arguments, the example must create an empty array, *emptyArgs*, with no elements.</span></span> <span data-ttu-id="10193-118">此範例會將輸入和輸出引數的這個陣列以及動作的名稱傳遞給 **InvokeAction** 。</span><span class="sxs-lookup"><span data-stu-id="10193-118">The example passes this array to **InvokeAction** for both the input and output arguments, along with the name of the action.</span></span>


```VB
Dim returnVal
Dim outArgs(1)
Dim args(1)
args(0) = 3
returnVal = service.InvokeAction("GetTrackInfo", args, outArgs)
'return Val now contains the track length
'and outArgs(0) contains the track title
Dim emptyArgs(0)
returnVal = service.InvokeAction("Play", emptyArgs, emptyArgs)
'returnVal indicates if the action was successful
```



## <a name="c-example"></a><span data-ttu-id="10193-119">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="10193-119">C++ Example</span></span>

<span data-ttu-id="10193-120">下列範例會定義 c + + 函式，此函式會叫用沒有引數的動作。</span><span class="sxs-lookup"><span data-stu-id="10193-120">The following example defines a C++ function that invokes an action with no arguments.</span></span> <span data-ttu-id="10193-121">由於 [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) 需要傳入的引數 [**safearray**](/windows/win32/api/oaidl/ns-oaidl-safearray) ，此範例會建立空的 **safearray**。</span><span class="sxs-lookup"><span data-stu-id="10193-121">Because [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of arguments to be passed in, this example creates an empty **SAFEARRAY**.</span></span> <span data-ttu-id="10193-122">因為此動作不會傳回值或具有 output 引數，所以這個範例會忽略傳遞給 **InvokeAction** 的最後兩個 [**變異**](/previous-versions/windows/desktop/automat/variant-manipulation-functions)值。</span><span class="sxs-lookup"><span data-stu-id="10193-122">Since this action does not return a value or have output arguments, this example ignores the last two [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) values passed to **InvokeAction**.</span></span>

<span data-ttu-id="10193-123">如果動作造成裝置的狀態變數變更，裝置會產生事件通知。</span><span class="sxs-lookup"><span data-stu-id="10193-123">The device generates event notifications if the action causes state variables of the device to change.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokePlay(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"Play");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 0;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            LONG    lStatus;
            VARIANT varInArgs;

            VariantInit(&varInArgs);

            varInArgs.vt = VT_VARIANT | VT_ARRAY;

            V_ARRAY(&varInArgs) = psa;

            hr = pService->InvokeAction(bstrActionName,
                                        varInArgs,
                                        NULL,
                                        NULL);

            if (SUCCEEDED(hr))
            {
                wcout << L"Action invoked successfully\n"; 
            }
            else
            {
                wcerr << L"Failed to invoke action - HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        

            }                                   

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



<span data-ttu-id="10193-124">下列範例會叫用虛構的 *GetTrackInfo* 動作。</span><span class="sxs-lookup"><span data-stu-id="10193-124">The following example invokes the fictitious *GetTrackInfo* action.</span></span> <span data-ttu-id="10193-125">它會將追蹤號碼當作引數，以傳回值的形式傳回曲目長度，並傳回輸出引數中的軌跡標題。</span><span class="sxs-lookup"><span data-stu-id="10193-125">It takes a track number as an argument, returns the track length as a return value, and returns the track title in an output argument.</span></span> <span data-ttu-id="10193-126">這段程式碼與上一個範例類似，不同之處在于，此範例不會建立輸入引數的空 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) ，而是會插入包含追蹤編號的 [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) 。</span><span class="sxs-lookup"><span data-stu-id="10193-126">The code is similar to the previous example, except that instead of creating an empty [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of input arguments, this example inserts a [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) that contains the track number.</span></span> <span data-ttu-id="10193-127">如果 [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) 傳回 success，此範例會檢查傳回值和 output 引數的陣列。</span><span class="sxs-lookup"><span data-stu-id="10193-127">If [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) returns success, this example examines the return value and the array of output arguments.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokeGetTrackInfo(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"GetTrackInfo");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 1;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            long rgIndices[1];
            VARIANT varTrackNum;

            rgIndices[0] = 0;
            VariantInit(&varTrackNum);

            varTrackNum.vt = VT_I4;
            // An arbitrary track is chosen (track 3)
            V_I4(&varTrackNum) = 3;

            hr = SafeArrayPutElement(psa,
                                     rgIndices,
                                     (void *) &varTrackNum);

            VariantClear(&varTrackNum);

            if (SUCCEEDED(hr))
            {            
                LONG    lStatus;
                VARIANT varInArgs;
                VARIANT varOutArgs;
                VARIANT varReturnVal;

                VariantInit(&varInArgs);
                VariantInit(&varOutArgs);
                VariantInit(&varReturnVal);

                varInArgs.vt = VT_VARIANT | VT_ARRAY;

                V_ARRAY(&varInArgs) = psa;

                hr = pService->InvokeAction(bstrActionName,
                                            varInArgs,
                                            &varOutArgs,
                                            &varReturnVal);

                if (SUCCEEDED(hr))
                {
                    SAFEARRAY * psaOutArgs = NULL;
                    VARIANT   varTrackTitle;

                    psaOutArgs = V_ARRAY(&varOutArgs);
                    VariantInit(&varTrackTitle);

                    rgIndices[0] = 0;
                    hr = SafeArrayGetElement(psaOutArgs,
                                             rgIndices,
                                             (void *)&varTrackTitle);                    

                    if (SUCCEEDED(hr))
                    {                    
                        wcout << L"Action invoked successfully\n"
                              << L"\tTrack Length == " 
                              << V_I4(&varReturnVal) << L"\n"
                              << L"\tTrack Title == " 
                              << V_BSTR(&varTrackTitle) << L"\n";
                    }
                    else
                    {
                        wcerr << L"Failed to get array element -"
                              << L" HRESULT 0x" 
                              << setbase(16)
                              << hr << L"\n";                        
                    }

                    VariantClear(&varTrackTitle);
                    VariantClear(&varReturnVal);
                    VariantClear(&varOutArgs);
                }
                else
                {
                    wcerr << L"Failed to invoke action - HRESULT 0x" 
                          << setbase(16)
                          << hr << L"\n";                        
                }                                   
            }
            else
            {
                wcerr << L"Failed to insert argument into array - "
                      << L"HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        
            }

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



 

 