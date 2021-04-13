---
description: '\_如果要複製的檔案是以 SP 複製 NOOVERWRITE 旗標排入佇列 \_ \_ ，而該檔案已存在於目標目錄中，則會將 SPFILENOTIFY TARGETEXISTS 通知傳送至回呼常式。'
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: 'SPFILENOTIFY_TARGETEXISTS 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386252"
---
# <a name="spfilenotify_targetexists-message"></a><span data-ttu-id="a9404-103">SPFILENOTIFY \_ TARGETEXISTS 訊息</span><span class="sxs-lookup"><span data-stu-id="a9404-103">SPFILENOTIFY\_TARGETEXISTS message</span></span>

<span data-ttu-id="a9404-104">如果要複製的檔案是以 SP 複製 NOOVERWRITE 旗標排入佇列，而該檔案已存在於目標目錄中，則會將 **SPFILENOTIFY \_ TARGETEXISTS** 通知傳送至回呼常式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="a9404-104">The **SPFILENOTIFY\_TARGETEXISTS** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NOOVERWRITE flag and that file already exists in the target directory.</span></span> <span data-ttu-id="a9404-105">您可以使用 OR 運算子，搭配 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) 和/或 [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) 通知，將它單獨傳送給回呼常式或合併使用。</span><span class="sxs-lookup"><span data-stu-id="a9404-105">It can be sent to the callback routine alone or combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md) notifications.</span></span>


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="a9404-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9404-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9404-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="a9404-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="a9404-108">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標，其中包含來源和目標檔案之路徑的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9404-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="a9404-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="a9404-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="a9404-110">除非使用 OR 運算子結合了 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) 通知，否則不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="a9404-110">This parameter is not used unless this notification is combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9404-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9404-111">Return value</span></span>

<span data-ttu-id="a9404-112">回呼常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a9404-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="a9404-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a9404-113">Return code</span></span>                                                                          | <span data-ttu-id="a9404-114">Description</span><span class="sxs-lookup"><span data-stu-id="a9404-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="a9404-115"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="a9404-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="a9404-116">覆寫目標目錄中的檔案。</span><span class="sxs-lookup"><span data-stu-id="a9404-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="a9404-117"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="a9404-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="a9404-118">略過目前的複製操作。</span><span class="sxs-lookup"><span data-stu-id="a9404-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="a9404-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9404-119">Requirements</span></span>



| <span data-ttu-id="a9404-120">需求</span><span class="sxs-lookup"><span data-stu-id="a9404-120">Requirement</span></span> | <span data-ttu-id="a9404-121">值</span><span class="sxs-lookup"><span data-stu-id="a9404-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9404-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9404-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9404-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9404-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a9404-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9404-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9404-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9404-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9404-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a9404-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9404-127"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9404-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9404-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9404-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9404-129">概觀</span><span class="sxs-lookup"><span data-stu-id="a9404-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="a9404-130">通知</span><span class="sxs-lookup"><span data-stu-id="a9404-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a9404-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="a9404-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="a9404-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="a9404-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="a9404-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="a9404-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="a9404-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="a9404-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="a9404-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="a9404-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="a9404-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="a9404-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




