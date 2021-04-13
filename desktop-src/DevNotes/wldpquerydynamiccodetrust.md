---
description: 抓取值，這個值會判斷指定的記憶體中或磁片上的 .NET CRL 動態程式碼是否受到 Device Guard 原則的信任。
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: 'WldpQueryDynamicCodeTrust 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510528"
---
# <a name="wldpquerydynamiccodetrust-function"></a><span data-ttu-id="dbf7c-103">WldpQueryDynamicCodeTrust 函式</span><span class="sxs-lookup"><span data-stu-id="dbf7c-103">WldpQueryDynamicCodeTrust function</span></span>

<span data-ttu-id="dbf7c-104">抓取值，這個值會判斷指定的記憶體中或磁片上的 .NET CRL 動態程式碼是否受到 Device Guard 原則的信任。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-104">Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="dbf7c-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a><span data-ttu-id="dbf7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="dbf7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf7c-107">*fileHandle*</span><span class="sxs-lookup"><span data-stu-id="dbf7c-107">*fileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="dbf7c-108">要檢查的磁片上動態程式碼檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-108">Handle to the on-disk dynamic code file to check.</span></span> <span data-ttu-id="dbf7c-109">如果 *fileHandle* 為非 **null**，則 *baseImage* 應該是 **null**。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-109">If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dbf7c-110">*baseImage*</span><span class="sxs-lookup"><span data-stu-id="dbf7c-110">*baseImage*</span></span> 
</dt> <dd>

<span data-ttu-id="dbf7c-111">要檢查之記憶體中 PE 檔案的指標。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-111">Pointer to the in-memory PE file to check.</span></span> <span data-ttu-id="dbf7c-112">如果 *baseImage* 為非 **null**，則 *FileHandle* 應該是 **null**。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-112">If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dbf7c-113">*ImageSize*</span><span class="sxs-lookup"><span data-stu-id="dbf7c-113">*ImageSize*</span></span> 
</dt> <dd>

<span data-ttu-id="dbf7c-114">當 *baseImage* 為非 **Null** 時，表示 *baseImage* 所指向的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-114">When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf7c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbf7c-115">Return value</span></span>

<span data-ttu-id="dbf7c-116">**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-116">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf7c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbf7c-117">Requirements</span></span>



| <span data-ttu-id="dbf7c-118">需求</span><span class="sxs-lookup"><span data-stu-id="dbf7c-118">Requirement</span></span> | <span data-ttu-id="dbf7c-119">值</span><span class="sxs-lookup"><span data-stu-id="dbf7c-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf7c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbf7c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf7c-121">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbf7c-121">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dbf7c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbf7c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf7c-123">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbf7c-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dbf7c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dbf7c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf7c-125"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf7c-125"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbf7c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf7c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf7c-127"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf7c-127"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




