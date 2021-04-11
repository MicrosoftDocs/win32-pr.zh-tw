---
description: SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO 通知會針對檔案佇列的複製子佇列中的每個節點 SetupScanFileQueue，傳送至回呼常式。
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: 'SPFILENOTIFY_QUEUESCAN_SIGNERINFO 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944608"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a><span data-ttu-id="224e3-103">SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="224e3-103">SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO message</span></span>

<span data-ttu-id="224e3-104">**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** 通知會針對檔案佇列的複製子佇列中的每個節點 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ，傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="224e3-104">The **SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="224e3-105">只有在呼叫 **SetupScanFileQueue** 函式來指定旗標 SPQ \_ SCAN \_ 使用 \_ 回呼 SIGNERINFO 時，才會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="224e3-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK\_SIGNERINFO.</span></span> <span data-ttu-id="224e3-106">從 Windows XP 開始提供。</span><span class="sxs-lookup"><span data-stu-id="224e3-106">Available starting with Windows XP.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="224e3-107">參數</span><span class="sxs-lookup"><span data-stu-id="224e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224e3-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="224e3-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="224e3-109">[**FILEPATHS \_ SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="224e3-109">Pointer to a [**FILEPATHS\_SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) structure.</span></span> <span data-ttu-id="224e3-110">**目標** 成員是系統上目標檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="224e3-110">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="224e3-111">**來源** 成員是原始程式檔的預期路徑。</span><span class="sxs-lookup"><span data-stu-id="224e3-111">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="224e3-112">**Win32Error** 成員是簽署錯誤。</span><span class="sxs-lookup"><span data-stu-id="224e3-112">The **Win32Error** member is the signing error.</span></span> <span data-ttu-id="224e3-113">如果回呼常式傳回 **Win32Error**= = NO ERROR，則會傳回簽章資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="224e3-113">Signature information is returned if the callback routine returns **Win32Error**==NO\_ERROR.</span></span> <span data-ttu-id="224e3-114">**DigitalSigner** 成員是數位簽章人。</span><span class="sxs-lookup"><span data-stu-id="224e3-114">The **DigitalSigner** member is the digital signer.</span></span> <span data-ttu-id="224e3-115">**版本** 成員為版本。</span><span class="sxs-lookup"><span data-stu-id="224e3-115">The **Version** member is the version.</span></span> <span data-ttu-id="224e3-116">**CatalogFile** 是類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="224e3-116">The **CatalogFile** is the catalog file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224e3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="224e3-117">Return value</span></span>

<span data-ttu-id="224e3-118">回呼常式應該會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="224e3-118">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="224e3-119">如果回呼常式未傳回 \_ 錯誤，則會繼續執行佇列掃描，如果常式傳回任何其他錯誤碼，則會傳回佇列掃描中止，且 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="224e3-119">If the callback routine returns NO\_ERROR, the queue scan continues, and returns If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="224e3-120">[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)函數不會處理這項通知。</span><span class="sxs-lookup"><span data-stu-id="224e3-120">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="224e3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="224e3-121">Requirements</span></span>



| <span data-ttu-id="224e3-122">需求</span><span class="sxs-lookup"><span data-stu-id="224e3-122">Requirement</span></span> | <span data-ttu-id="224e3-123">值</span><span class="sxs-lookup"><span data-stu-id="224e3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="224e3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="224e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="224e3-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="224e3-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="224e3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="224e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="224e3-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="224e3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="224e3-128">標頭</span><span class="sxs-lookup"><span data-stu-id="224e3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="224e3-129"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="224e3-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="224e3-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="224e3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224e3-131">概觀</span><span class="sxs-lookup"><span data-stu-id="224e3-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="224e3-132">通知</span><span class="sxs-lookup"><span data-stu-id="224e3-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="224e3-133">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="224e3-133">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

