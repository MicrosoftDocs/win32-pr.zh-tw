---
description: 抓取特定 Microsoft .NET Passport 登入選項的值。
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: IPassportManager3：： get_Option 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385860"
---
# <a name="ipassportmanager3get_option-method"></a><span data-ttu-id="1e559-103">IPassportManager3：： get \_ 選項方法</span><span class="sxs-lookup"><span data-stu-id="1e559-103">IPassportManager3::get\_Option method</span></span>

<span data-ttu-id="1e559-104">抓取特定 Microsoft .NET Passport 登入選項的值。</span><span class="sxs-lookup"><span data-stu-id="1e559-104">Retrieves the value of a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="1e559-105">**Get \_ 選項** 方法屬於 [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10))介面。</span><span class="sxs-lookup"><span data-stu-id="1e559-105">The **get\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="1e559-106">本主題補充最初的檔。</span><span class="sxs-lookup"><span data-stu-id="1e559-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1e559-107">語法</span><span class="sxs-lookup"><span data-stu-id="1e559-107">Syntax</span></span>


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1e559-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e559-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e559-109">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e559-109">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e559-110">要取出的登入選項。</span><span class="sxs-lookup"><span data-stu-id="1e559-110">The sign-in option to be retrieved.</span></span> <span data-ttu-id="1e559-111">目前唯一支援的選項是 "iMode"。</span><span class="sxs-lookup"><span data-stu-id="1e559-111">Currently, the only supported option is "iMode".</span></span>

</dd> <dt>

<span data-ttu-id="1e559-112">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1e559-112">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e559-113">**變數** 的指標， (VT \_ BOOL) ，可接收選項的值。</span><span class="sxs-lookup"><span data-stu-id="1e559-113">A pointer to a **VARIANT** (VT\_BOOL) that receives the value of the option.</span></span> <span data-ttu-id="1e559-114">這個值可以是 True 或 False。</span><span class="sxs-lookup"><span data-stu-id="1e559-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e559-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e559-115">Return value</span></span>

<span data-ttu-id="1e559-116">\_當方法成功時傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="1e559-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e559-117">備註</span><span class="sxs-lookup"><span data-stu-id="1e559-117">Remarks</span></span>

<span data-ttu-id="1e559-118">此方法隨附于較舊版本的 Passport SDK。</span><span class="sxs-lookup"><span data-stu-id="1e559-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
