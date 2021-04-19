---
description: INonDelegatingUnknown 介面是已重新命名的 IUnknown 版本，可支援 nondelegating 和委派相同 COM 物件中的 IUnknown 介面。
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: 'INonDelegatingUnknown (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993226"
---
# <a name="inondelegatingunknown"></a><span data-ttu-id="d3bd7-103">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="d3bd7-103">INonDelegatingUnknown</span></span>

<span data-ttu-id="d3bd7-104">`INonDelegatingUnknown`介面是已重新命名的 **IUnknown** 版本，可支援 nondelegating 以及在相同的 COM 物件中委派 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-104">The `INonDelegatingUnknown` interface is a version of **IUnknown** that is renamed to enable support for both nondelegating and delegating **IUnknown** interfaces in the same COM object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3bd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3bd7-105">Syntax</span></span>


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a><span data-ttu-id="d3bd7-106">備註</span><span class="sxs-lookup"><span data-stu-id="d3bd7-106">Remarks</span></span>

<span data-ttu-id="d3bd7-107">若要使用 `INonDelegatingUnknown` 多重繼承，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-107">To use `INonDelegatingUnknown` for multiple inheritance, perform the following steps.</span></span>

1.  <span data-ttu-id="d3bd7-108">從介面衍生您的類別，例如 IMyInterface。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-108">Derive your class from an interface, for example, IMyInterface.</span></span>
2.  <span data-ttu-id="d3bd7-109">在您的類別定義中包含 [**declare \_ IUNKNOWN**](declare-iunknown.md) ，以宣告呼叫外部未知之 **QueryInterface**、 **AddRef** 和 **Release** 的實部。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-109">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition to declare implementations of **QueryInterface**, **AddRef**, and **Release** that call the outer unknown.</span></span>
3.  <span data-ttu-id="d3bd7-110">覆寫 **NonDelegatingQueryInterface** 以公開具有下列程式碼的 IMyInterface：</span><span class="sxs-lookup"><span data-stu-id="d3bd7-110">Override **NonDelegatingQueryInterface** to expose IMyInterface with code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="d3bd7-111">宣告和執行 IMyInterface 的成員函式。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-111">Declare and implement the member functions of IMyInterface.</span></span>

<span data-ttu-id="d3bd7-112">若要使用 `INonDelegatingUnknown` 于嵌套介面，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d3bd7-112">To use `INonDelegatingUnknown` for nested interfaces, perform the following steps:</span></span>

1.  <span data-ttu-id="d3bd7-113">宣告衍生自 [**CUnknown**](cunknown.md)的類別。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-113">Declare a class derived from [**CUnknown**](cunknown.md).</span></span>
2.  <span data-ttu-id="d3bd7-114">在您的類別定義中包含 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-114">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition.</span></span>
3.  <span data-ttu-id="d3bd7-115">覆寫 **NonDelegatingQueryInterface** 以使用下列程式碼來公開 IMyInterface：</span><span class="sxs-lookup"><span data-stu-id="d3bd7-115">Override **NonDelegatingQueryInterface** to expose IMyInterface with the code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="d3bd7-116">執行 IMyInterface 的成員函式。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-116">Implement the member functions of IMyInterface.</span></span> <span data-ttu-id="d3bd7-117">使用 [**CUnknown：： GetOwner**](cunknown-getowner.md) 存取 COM 物件類別。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-117">Use [**CUnknown::GetOwner**](cunknown-getowner.md) to access the COM object class.</span></span>
5.  <span data-ttu-id="d3bd7-118">在您的 COM 物件類別中，將嵌套類別設為 COM 物件類別的 friend，然後將嵌套類別的實例宣告為 COM 物件類別的成員。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-118">In your COM object class, make the nested class a friend of the COM object class, and declare an instance of the nested class as a member of the COM object class.</span></span>

<span data-ttu-id="d3bd7-119">因為您必須一律將外部未知和 **HRESULT** 傳遞給 [**CUnknown**](cunknown.md) 的函式，所以您無法使用預設的函式。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-119">Because you must always pass the outer unknown and an **HRESULT** to the [**CUnknown**](cunknown.md) constructor, you can't use a default constructor.</span></span> <span data-ttu-id="d3bd7-120">您必須讓成員變數成為類別的指標，並在您的函式中進行新的呼叫，以實際建立它。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-120">You have to make the member variable a pointer to the class and make a new call in your constructor to actually create it.</span></span>

<span data-ttu-id="d3bd7-121">使用下列程式碼覆寫 **NonDelegatingQueryInterface** ：</span><span class="sxs-lookup"><span data-stu-id="d3bd7-121">Override the **NonDelegatingQueryInterface** with code such as the following:</span></span>


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



<span data-ttu-id="d3bd7-122">您可以有混合類別，透過多個繼承和一些介面（透過嵌套類別）來支援某些介面。</span><span class="sxs-lookup"><span data-stu-id="d3bd7-122">You can have mixed classes that support some interfaces through multiple inheritance and some interfaces through nested classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3bd7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3bd7-123">Requirements</span></span>



| <span data-ttu-id="d3bd7-124">需求</span><span class="sxs-lookup"><span data-stu-id="d3bd7-124">Requirement</span></span> | <span data-ttu-id="d3bd7-125">值</span><span class="sxs-lookup"><span data-stu-id="d3bd7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3bd7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d3bd7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d3bd7-127"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d3bd7-127"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3bd7-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3bd7-128">Library</span></span><br/> | <dl> <span data-ttu-id="d3bd7-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d3bd7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3bd7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3bd7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3bd7-131">**COM Helper 函數**</span><span class="sxs-lookup"><span data-stu-id="d3bd7-131">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




