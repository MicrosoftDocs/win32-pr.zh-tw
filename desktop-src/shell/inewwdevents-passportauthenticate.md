---
description: 在嚮導中啟用裝載的伺服器端頁面，以確認使用者已通過 Microsoft 帳戶驗證。
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: 'NewWDEvents. PassportAuthenticate 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695651"
---
# <a name="newwdeventspassportauthenticate-method"></a><span data-ttu-id="90715-103">NewWDEvents. PassportAuthenticate 方法</span><span class="sxs-lookup"><span data-stu-id="90715-103">NewWDEvents.PassportAuthenticate method</span></span>

<span data-ttu-id="90715-104">在嚮導中啟用裝載的伺服器端頁面，以確認使用者已通過 Microsoft 帳戶驗證。</span><span class="sxs-lookup"><span data-stu-id="90715-104">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="syntax"></a><span data-ttu-id="90715-105">語法</span><span class="sxs-lookup"><span data-stu-id="90715-105">Syntax</span></span>


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a><span data-ttu-id="90715-106">參數</span><span class="sxs-lookup"><span data-stu-id="90715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90715-107">*bstrSignInUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90715-107">*bstrSignInUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90715-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="90715-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="90715-109">字串，包含重新導向至 Microsoft 帳戶的登入 UI 之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="90715-109">A string containing the URL of a webpage that redirects to the Microsoft account log on UI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90715-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="90715-110">Return value</span></span>

<span data-ttu-id="90715-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="90715-111">Type: **Boolean**</span></span>

<span data-ttu-id="90715-112">如果驗證成功，則設定為 **true** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="90715-112">Set to **true** if authentication succeeds, **false** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="90715-113">備註</span><span class="sxs-lookup"><span data-stu-id="90715-113">Remarks</span></span>

<span data-ttu-id="90715-114">即使使用者已登入 Microsoft 帳戶，也可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="90715-114">This method may be called even if a user is already logged on to a Microsoft account.</span></span> <span data-ttu-id="90715-115">在此情況下，方法會傳回 **true** ，而不會在 UI 上顯示 Microsoft 帳戶的登入。</span><span class="sxs-lookup"><span data-stu-id="90715-115">In that case, the method returns **true** without displaying the Microsoft account log on UI.</span></span>

## <a name="requirements"></a><span data-ttu-id="90715-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="90715-116">Requirements</span></span>



| <span data-ttu-id="90715-117">需求</span><span class="sxs-lookup"><span data-stu-id="90715-117">Requirement</span></span> | <span data-ttu-id="90715-118">值</span><span class="sxs-lookup"><span data-stu-id="90715-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90715-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90715-119">Minimum supported client</span></span><br/> | <span data-ttu-id="90715-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90715-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="90715-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90715-121">Minimum supported server</span></span><br/> | <span data-ttu-id="90715-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90715-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="90715-123">標頭</span><span class="sxs-lookup"><span data-stu-id="90715-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90715-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="90715-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="90715-125">Idl</span><span class="sxs-lookup"><span data-stu-id="90715-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90715-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="90715-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="90715-127">DLL</span><span class="sxs-lookup"><span data-stu-id="90715-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90715-128"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="90715-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
