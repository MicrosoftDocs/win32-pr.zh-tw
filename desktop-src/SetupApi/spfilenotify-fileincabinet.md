---
description: 針對封 \_ 包中找到的每個檔案，SetupIterateCabinet 會將 SPFILENOTIFY FILEINCABINET 通知傳送至回呼常式。 回呼常式必須傳回值，指出是否要解壓縮檔案。
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: 'SPFILENOTIFY_FILEINCABINET 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000331"
---
# <a name="spfilenotify_fileincabinet-message"></a><span data-ttu-id="ea7c8-104">SPFILENOTIFY \_ FILEINCABINET 訊息</span><span class="sxs-lookup"><span data-stu-id="ea7c8-104">SPFILENOTIFY\_FILEINCABINET message</span></span>

<span data-ttu-id="ea7c8-105">針對封包中找到的每個檔案， [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)會將 **SPFILENOTIFY \_ FILEINCABINET** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-105">The **SPFILENOTIFY\_FILEINCABINET** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) for each file found in the cabinet.</span></span> <span data-ttu-id="ea7c8-106">回呼常式必須傳回值，指出是否要解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-106">The callback routine must return a value indicating whether to extract the file.</span></span>


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a><span data-ttu-id="ea7c8-107">參數</span><span class="sxs-lookup"><span data-stu-id="ea7c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea7c8-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="ea7c8-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="ea7c8-109">封 [**\_ \_ 包 \_ 資訊結構中檔案**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) 的指標，其中包含封包中檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-109">Pointer to a [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure that contains information about the file in the cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="ea7c8-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="ea7c8-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="ea7c8-111">以 null 結束的字串指標，其中包含封包檔的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-111">Pointer to a null-terminated string that contains the filename of the cabinet file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea7c8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea7c8-112">Return value</span></span>

<span data-ttu-id="ea7c8-113">您的回呼常式應該會傳回下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-113">Your callback routine should return one of the following.</span></span>



| <span data-ttu-id="ea7c8-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea7c8-114">Return code</span></span>                                                                                 | <span data-ttu-id="ea7c8-115">Description</span><span class="sxs-lookup"><span data-stu-id="ea7c8-115">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ea7c8-116"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="ea7c8-116"><dt>**FILEOP\_SKIP**</dt></span></span> </dl> | <span data-ttu-id="ea7c8-117">不要解壓縮檔案，請略過。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-117">Do not extract the file, skip it.</span></span><br/> |
| <dl> <span data-ttu-id="ea7c8-118"><dt>**FILEOP \_ DOIT R**</dt></span><span class="sxs-lookup"><span data-stu-id="ea7c8-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl> | <span data-ttu-id="ea7c8-119">將檔案解壓縮。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-119">Extract the file.</span></span><br/>                 |



 

<span data-ttu-id="ea7c8-120">如果您的回呼常式 \_ 傳回 FILEOP doit r，則要用於解壓縮檔案的名稱應該在封 [**\_ \_ 包 \_ 資訊**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)結構中傳遞至 *Param1* 的常式之檔案的 **FullTargetName** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-120">If your callback routine returns FILEOP\_DOIT, the name to use for the extracted file should be specified in the **FullTargetName** member of the [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure passed to the routine in *Param1*.</span></span>

> [!Note]  
> <span data-ttu-id="ea7c8-121">沒有預設的封包回呼常式。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-121">There is no default cabinet callback routine.</span></span> <span data-ttu-id="ea7c8-122">安裝應用程式應該提供回呼常式來處理 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="ea7c8-122">The setup application should supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea7c8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea7c8-123">Requirements</span></span>



| <span data-ttu-id="ea7c8-124">需求</span><span class="sxs-lookup"><span data-stu-id="ea7c8-124">Requirement</span></span> | <span data-ttu-id="ea7c8-125">值</span><span class="sxs-lookup"><span data-stu-id="ea7c8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea7c8-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea7c8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea7c8-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea7c8-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ea7c8-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea7c8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea7c8-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea7c8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea7c8-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ea7c8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea7c8-131"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea7c8-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea7c8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea7c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea7c8-133">概觀</span><span class="sxs-lookup"><span data-stu-id="ea7c8-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="ea7c8-134">通知</span><span class="sxs-lookup"><span data-stu-id="ea7c8-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="ea7c8-135">**封 \_ 包資訊中的 \_ 檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="ea7c8-135">**FILE\_IN\_CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="ea7c8-136">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="ea7c8-136">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




