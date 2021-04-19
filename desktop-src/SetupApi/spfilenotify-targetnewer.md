---
description: '\_如果要複製的檔案已排入較新的 sp \_ 複製 \_ ，或是 sp \_ copy \_ 強制 \_ 指定較新的旗標，且目標目錄中已有較新版本的檔案，則會將 SPFILENOTIFY TARGETNEWER 通知傳送至回呼常式。'
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: 'SPFILENOTIFY_TARGETNEWER 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993199"
---
# <a name="spfilenotify_targetnewer-message"></a><span data-ttu-id="419e3-103">SPFILENOTIFY \_ TARGETNEWER 訊息</span><span class="sxs-lookup"><span data-stu-id="419e3-103">SPFILENOTIFY\_TARGETNEWER message</span></span>

<span data-ttu-id="419e3-104">如果 **要 \_** 複製的檔案已排入較新的 sp \_ 複製 \_ ，或是 sp \_ copy \_ 強制 \_ 指定較新的旗標，且目標目錄中已有較新版本的檔案，則會將 SPFILENOTIFY TARGETNEWER 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="419e3-104">The **SPFILENOTIFY\_TARGETNEWER** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NEWER or SP\_COPY\_FORCE\_NEWER flags specified and a newer version of the file already exists in the target directory.</span></span> <span data-ttu-id="419e3-105">它可以單獨傳送給回呼常式，或與 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) 和/或 [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)一起 or 運算。</span><span class="sxs-lookup"><span data-stu-id="419e3-105">It can be sent to the callback routine alone or ORed together with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md).</span></span>


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="419e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="419e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="419e3-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="419e3-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="419e3-108">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標，其中包含來源和目標檔案之路徑的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="419e3-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="419e3-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="419e3-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="419e3-110">除非使用 OR 運算子搭配 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)來合併此通知，否則不會使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="419e3-110">This parameter is not used unless this notification is combined, by using the OR operator, with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="419e3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="419e3-111">Return value</span></span>

<span data-ttu-id="419e3-112">回呼常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="419e3-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="419e3-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="419e3-113">Return code</span></span>                                                                          | <span data-ttu-id="419e3-114">Description</span><span class="sxs-lookup"><span data-stu-id="419e3-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="419e3-115"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="419e3-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="419e3-116">覆寫目標目錄中的檔案。</span><span class="sxs-lookup"><span data-stu-id="419e3-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="419e3-117"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="419e3-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="419e3-118">略過目前的複製操作。</span><span class="sxs-lookup"><span data-stu-id="419e3-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="419e3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="419e3-119">Requirements</span></span>



| <span data-ttu-id="419e3-120">需求</span><span class="sxs-lookup"><span data-stu-id="419e3-120">Requirement</span></span> | <span data-ttu-id="419e3-121">值</span><span class="sxs-lookup"><span data-stu-id="419e3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="419e3-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="419e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="419e3-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="419e3-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="419e3-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="419e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="419e3-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="419e3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="419e3-126">標頭</span><span class="sxs-lookup"><span data-stu-id="419e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="419e3-127"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="419e3-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="419e3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="419e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419e3-129">概觀</span><span class="sxs-lookup"><span data-stu-id="419e3-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="419e3-130">通知</span><span class="sxs-lookup"><span data-stu-id="419e3-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="419e3-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="419e3-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="419e3-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="419e3-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="419e3-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="419e3-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="419e3-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="419e3-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="419e3-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="419e3-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="419e3-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="419e3-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




