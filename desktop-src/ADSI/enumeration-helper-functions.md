---
title: 列舉 Helper 函數
description: 有三個可從 C/c + + 使用的列舉值協助程式函式，可協助 Active Directory 物件的導覽。 它們是 ADsBuildEnumerator、ADsEnumerateNext 和 ADsFreeEnumerator。
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- 使用 ADsBuildEnumerator ADSI
- 使用 ADsEnumerateNext ADSI
- 使用 ADsFreeEnumerator ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 ADsBuildEnumerator ADsEnumerateNext 和 ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9597787202adf183435262eab9341957e19457
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093296"
---
# <a name="enumeration-helper-functions"></a><span data-ttu-id="1f252-108">列舉 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="1f252-108">Enumeration Helper Functions</span></span>

<span data-ttu-id="1f252-109">有三個可從 C/c + + 使用的列舉值協助程式函式，可協助 Active Directory 物件的導覽。</span><span class="sxs-lookup"><span data-stu-id="1f252-109">There are three enumerator helper functions that can be used from C/C++ to aid in the navigation of Active Directory objects.</span></span> <span data-ttu-id="1f252-110">它們是 [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)、 [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)和 [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)。</span><span class="sxs-lookup"><span data-stu-id="1f252-110">They are [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext), and [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span></span>

## <a name="adsbuildenumerator"></a><span data-ttu-id="1f252-111">ADsBuildEnumerator</span><span class="sxs-lookup"><span data-stu-id="1f252-111">ADsBuildEnumerator</span></span>

<span data-ttu-id="1f252-112">[**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) helper 函數會封裝建立列舉值物件所需的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1f252-112">The [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) helper function encapsulates the code required to create an enumerator object.</span></span> <span data-ttu-id="1f252-113">它會呼叫 [**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)方法來建立列舉值物件，然後呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，以取得該物件的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面指標。</span><span class="sxs-lookup"><span data-stu-id="1f252-113">It calls the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) method to create an enumerator object and then calls the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to get a pointer to the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface for that object.</span></span> <span data-ttu-id="1f252-114">列舉物件是可列舉容器的自動化機制。</span><span class="sxs-lookup"><span data-stu-id="1f252-114">The enumeration object is the Automation mechanism to enumerate over containers.</span></span> <span data-ttu-id="1f252-115">使用 [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) 函式釋放這個列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="1f252-115">Use the [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) function to release this enumerator object.</span></span>

## <a name="adsenumeratenext"></a><span data-ttu-id="1f252-116">ADsEnumerateNext</span><span class="sxs-lookup"><span data-stu-id="1f252-116">ADsEnumerateNext</span></span>

<span data-ttu-id="1f252-117">[**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) helper 函式會使用從列舉值物件提取的元素來擴展 VARIANT 陣列。</span><span class="sxs-lookup"><span data-stu-id="1f252-117">The [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) helper function populates a VARIANT array with elements fetched from an enumerator object.</span></span> <span data-ttu-id="1f252-118">抓取的元素數目可以小於要求的數目。</span><span class="sxs-lookup"><span data-stu-id="1f252-118">The number of elements retrieved can be smaller than the number requested.</span></span>

## <a name="adsfreeenumerator"></a><span data-ttu-id="1f252-119">ADsFreeEnumerator</span><span class="sxs-lookup"><span data-stu-id="1f252-119">ADsFreeEnumerator</span></span>

<span data-ttu-id="1f252-120">釋放先前透過 [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) 函數建立的列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="1f252-120">Frees an enumerator object previously created through the [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) function.</span></span>

<span data-ttu-id="1f252-121">下列程式碼範例顯示在 c + + 中使用列舉值協助程式函式的函式。</span><span class="sxs-lookup"><span data-stu-id="1f252-121">The following code example shows a function that uses enumerator helper functions in C++.</span></span>


```C++
/*****************************************************************************
  Function:    TestEnumObject
  Arguments:   pszADsPath - ADsPath of the container to be enumerated (WCHAR*).
  Return:      S_OK if successful, an error code otherwise.
  Purpose:     Example using ADsBuildEnumerator, ADsEnumerateNext and
               ADsFreeEnumerator.
******************************************************************************/
#define MAX_ENUM      100  
 
HRESULT
TestEnumObject( LPWSTR pszADsPath )
{
    ULONG cElementFetched = 0L;
    IEnumVARIANT * pEnumVariant = NULL;
    VARIANT VariantArray[MAX_ENUM];
    HRESULT hr = S_OK;
    IADsContainer * pADsContainer =  NULL;
    DWORD dwObjects = 0, dwEnumCount = 0, i = 0;
    BOOL  fContinue = TRUE;
 
 
    hr = ADsGetObject(
                pszADsPath,
                IID_IADsContainer,
                (void **)&pADsContainer
                );
 
 
    if (FAILED(hr)) {
 
        printf("\"%S\" is not a valid container object.\n", pszADsPath) ;
        goto exitpoint ;
    }
 
    hr = ADsBuildEnumerator(
            pADsContainer,
            &pEnumVariant
            );
 
    if( FAILED( hr ) )
    {
      printf("ADsBuildEnumerator failed with %lx\n", hr ) ;
      goto exitpoint ;
    }
 
    fContinue  = TRUE;
    while (fContinue) {
 
        IADs *pObject ;
 
        hr = ADsEnumerateNext(
                    pEnumVariant,
                    MAX_ENUM,
                    VariantArray,
                    &cElementFetched
                    );

        if ( FAILED( hr ) )
        {
            printf("ADsEnumerateNext failed with %lx\n",hr);
            goto exitpoint;
        }
 
        if (hr == S_FALSE) {
            fContinue = FALSE;
        }
 
        dwEnumCount++;
 
        for (i = 0; i < cElementFetched; i++ ) {
 
            IDispatch *pDispatch    = NULL;
            BSTR        bstrADsPath = NULL;
 
            pDispatch = VariantArray[i].pdispVal;
 
            hr = V_DISPATCH( VariantArray + i )->QueryInterface(IID_IADs, (void **) &pObject) ;
 
            if( SUCCEEDED( hr ) )
            {
               pObject->get_ADsPath( &bstrADsPath );
               printf( "%S\n", bstrADsPath );
            }
            pObject->Release();
            VariantClear( VariantArray + i );
            SysFreeString( bstrADsPath );
        }
 
        dwObjects += cElementFetched;
    }
 
    printf("Total Number of Objects enumerated is %d\n", dwObjects);
 
exitpoint:
    if (pEnumVariant) {
        ADsFreeEnumerator( pEnumVariant );
    }
 
    if (pADsContainer) {
        pADsContainer->Release();
    }
 
    return(hr);
}
```



 

 