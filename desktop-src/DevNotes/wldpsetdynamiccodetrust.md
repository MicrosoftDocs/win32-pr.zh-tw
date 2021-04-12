---
description: 為 .NET 設定磁片上的 .NET CRL 動態程式碼信任。
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: 'WldpSetDynamicCodeTrust 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385906"
---
# <a name="wldpsetdynamiccodetrust-function"></a><span data-ttu-id="568e0-103">WldpSetDynamicCodeTrust 函式</span><span class="sxs-lookup"><span data-stu-id="568e0-103">WldpSetDynamicCodeTrust function</span></span>

<span data-ttu-id="568e0-104">為 .NET 設定磁片上的 .NET CRL 動態程式碼信任。</span><span class="sxs-lookup"><span data-stu-id="568e0-104">Sets an on-disk .NET CRL Dynamic Code trustable for .NET.</span></span>

## <a name="syntax"></a><span data-ttu-id="568e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="568e0-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a><span data-ttu-id="568e0-106">參數</span><span class="sxs-lookup"><span data-stu-id="568e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="568e0-107">*FileHandle*</span><span class="sxs-lookup"><span data-stu-id="568e0-107">*FileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="568e0-108">磁片上動態程式碼檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="568e0-108">Handle to a on-disk dynamic code file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="568e0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="568e0-109">Return value</span></span>

<span data-ttu-id="568e0-110">**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="568e0-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="568e0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="568e0-111">Requirements</span></span>



| <span data-ttu-id="568e0-112">需求</span><span class="sxs-lookup"><span data-stu-id="568e0-112">Requirement</span></span> | <span data-ttu-id="568e0-113">值</span><span class="sxs-lookup"><span data-stu-id="568e0-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="568e0-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="568e0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="568e0-115">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="568e0-115">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="568e0-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="568e0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="568e0-117">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="568e0-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="568e0-118">標頭</span><span class="sxs-lookup"><span data-stu-id="568e0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="568e0-119"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="568e0-119"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="568e0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="568e0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="568e0-121"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="568e0-121"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




