---
title: IADsExtension 介面
description: 本主題包含使用 IADsExtension 介面的 c + + 程式碼範例。
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- 使用 IADsExtension ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 IADsExtension
- 延伸模組 ADSI、IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683089"
---
# <a name="iadsextension-interface"></a><span data-ttu-id="4be06-106">IADsExtension 介面</span><span class="sxs-lookup"><span data-stu-id="4be06-106">IADsExtension Interface</span></span>

<span data-ttu-id="4be06-107">[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)介面的定義如下：</span><span class="sxs-lookup"><span data-stu-id="4be06-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



<span data-ttu-id="4be06-108">ADSI) 的匯總工具 (會呼叫 [**IADsExtension：：操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) 方法。</span><span class="sxs-lookup"><span data-stu-id="4be06-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="4be06-109">擴充功能應該根據提供者的檔，來解讀 *dwCode* 參數和每個 *varData* 參數。</span><span class="sxs-lookup"><span data-stu-id="4be06-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="4be06-110"> (ADSI) 的匯總工具，會呼叫 [**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) 方法。</span><span class="sxs-lookup"><span data-stu-id="4be06-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="4be06-111">它是在 ADSI 決定服務分派的延伸模組之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="4be06-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="4be06-112">延伸模組可以使用型別資訊來取得 DISPID，也就是使用 [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) 函數。</span><span class="sxs-lookup"><span data-stu-id="4be06-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="4be06-113">ADSI 通常會在呼叫 [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)函數之後呼叫 [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke)方法。</span><span class="sxs-lookup"><span data-stu-id="4be06-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="4be06-114">擴充功能應該呼叫它所執行的實際方法。</span><span class="sxs-lookup"><span data-stu-id="4be06-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="4be06-115">或者，擴充功能可以使用類型資訊，並呼叫 [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) 函式。</span><span class="sxs-lookup"><span data-stu-id="4be06-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="4be06-116">所有參數的意義與標準 [**IDispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 方法中的參數相同。</span><span class="sxs-lookup"><span data-stu-id="4be06-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 