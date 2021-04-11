---
description: 確認 DVD 光碟機中的媒體區域與 DVD 光碟機區域相符。
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111176"
---
# <a name="dvdlauncher-function"></a><span data-ttu-id="235cf-103">DvdLauncher 函式</span><span class="sxs-lookup"><span data-stu-id="235cf-103">DvdLauncher function</span></span>

<span data-ttu-id="235cf-104">確認 DVD 光碟機中的媒體區域與 DVD 光碟機區域相符。</span><span class="sxs-lookup"><span data-stu-id="235cf-104">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>

## <a name="syntax"></a><span data-ttu-id="235cf-105">語法</span><span class="sxs-lookup"><span data-stu-id="235cf-105">Syntax</span></span>


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="235cf-106">參數</span><span class="sxs-lookup"><span data-stu-id="235cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235cf-107">*HWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="235cf-107">*HWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235cf-108">最上層視窗的控制碼，可用於任何必要的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="235cf-108">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="235cf-109">*R* \[在\]</span><span class="sxs-lookup"><span data-stu-id="235cf-109">*DriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235cf-110">磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="235cf-110">The drive letter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235cf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="235cf-111">Return value</span></span>

<span data-ttu-id="235cf-112">如果函數成功且區域相符，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="235cf-112">If the function succeeds and the regions match, the return value is nonzero.</span></span> <span data-ttu-id="235cf-113">否則，傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="235cf-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="235cf-114">備註</span><span class="sxs-lookup"><span data-stu-id="235cf-114">Remarks</span></span>

<span data-ttu-id="235cf-115">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="235cf-115">This function has no associated import library.</span></span> <span data-ttu-id="235cf-116">您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 StorProp.dll。</span><span class="sxs-lookup"><span data-stu-id="235cf-116">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to StorProp.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="235cf-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="235cf-117">Requirements</span></span>



| <span data-ttu-id="235cf-118">需求</span><span class="sxs-lookup"><span data-stu-id="235cf-118">Requirement</span></span> | <span data-ttu-id="235cf-119">值</span><span class="sxs-lookup"><span data-stu-id="235cf-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="235cf-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="235cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="235cf-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="235cf-121">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="235cf-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="235cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="235cf-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="235cf-123">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="235cf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="235cf-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="235cf-125"><dt>StorProp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235cf-125"><dt>StorProp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235cf-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="235cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235cf-127">裝置管理函式</span><span class="sxs-lookup"><span data-stu-id="235cf-127">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

