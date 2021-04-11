---
description: 設定特定的 Microsoft .NET Passport 登入選項。
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3：:p ut_Option 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936084"
---
# <a name="ipassportmanager3put_option-method"></a><span data-ttu-id="9c522-103">IPassportManager3：:p 的 \_ 選項方法</span><span class="sxs-lookup"><span data-stu-id="9c522-103">IPassportManager3::put\_Option method</span></span>

<span data-ttu-id="9c522-104">設定特定的 Microsoft .NET Passport 登入選項。</span><span class="sxs-lookup"><span data-stu-id="9c522-104">Sets a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="9c522-105">**Put \_ 選項** 方法屬於 [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10))介面。</span><span class="sxs-lookup"><span data-stu-id="9c522-105">The **put\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="9c522-106">本主題補充最初的檔。</span><span class="sxs-lookup"><span data-stu-id="9c522-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9c522-107">語法</span><span class="sxs-lookup"><span data-stu-id="9c522-107">Syntax</span></span>


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="9c522-108">參數</span><span class="sxs-lookup"><span data-stu-id="9c522-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c522-109">*name*</span><span class="sxs-lookup"><span data-stu-id="9c522-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="9c522-110">要設定的登入選項。</span><span class="sxs-lookup"><span data-stu-id="9c522-110">The sign-in option to be set.</span></span> <span data-ttu-id="9c522-111">目前唯一支援的選項為 iMode。</span><span class="sxs-lookup"><span data-stu-id="9c522-111">Currently, the only supported option is iMode.</span></span>

</dd> <dt>

<span data-ttu-id="9c522-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="9c522-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="9c522-113"> ( VT \_ BOOL) 的 VARIANT，可指定選項的新值。</span><span class="sxs-lookup"><span data-stu-id="9c522-113">A **VARIANT** (VT\_BOOL) that specifies the new value for the option.</span></span> <span data-ttu-id="9c522-114">這個值可以是 True 或 False。</span><span class="sxs-lookup"><span data-stu-id="9c522-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c522-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c522-115">Return value</span></span>

<span data-ttu-id="9c522-116">\_當方法成功時傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="9c522-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c522-117">備註</span><span class="sxs-lookup"><span data-stu-id="9c522-117">Remarks</span></span>

<span data-ttu-id="9c522-118">此方法隨附于較舊版本的 Passport SDK。</span><span class="sxs-lookup"><span data-stu-id="9c522-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
