---
description: '\_如果要複製之檔案的語言不符合現有目標檔案的語言，則會將 SPFILENOTIFY LANGMISMATCH 通知傳送至回呼常式。'
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: 'SPFILENOTIFY_LANGMISMATCH 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979384"
---
# <a name="spfilenotify_langmismatch-message"></a><span data-ttu-id="4c2f0-103">SPFILENOTIFY \_ LANGMISMATCH 訊息</span><span class="sxs-lookup"><span data-stu-id="4c2f0-103">SPFILENOTIFY\_LANGMISMATCH message</span></span>

<span data-ttu-id="4c2f0-104">如果要複製之檔案的語言不符合現有目標檔案的語言，則會將 **SPFILENOTIFY \_ LANGMISMATCH** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-104">The **SPFILENOTIFY\_LANGMISMATCH** notification is sent to the callback routine if the language of the file to be copied does not match the language of an existing target file.</span></span> <span data-ttu-id="4c2f0-105">您可以使用 OR 運算子，搭配 [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) 和/或 [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)，將它單獨傳送給回呼常式或結合。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-105">It can be sent to the callback routine alone or combined, by using the OR operator, with [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md).</span></span>


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="4c2f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c2f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c2f0-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="4c2f0-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="4c2f0-108">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標，其中包含來源和目標檔案路徑的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths of the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="4c2f0-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="4c2f0-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="4c2f0-110">識別不相符的語言。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-110">Identifies the mismatched languages.</span></span> <span data-ttu-id="4c2f0-111">此成員具有低字組中原始程式檔的語言識別項，以及最高單字中現有目標檔案的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-111">This member has the language identifier of the source file in the low word, and the language identifier of the existing target file in the high word.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c2f0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c2f0-112">Return value</span></span>

<span data-ttu-id="4c2f0-113">回呼常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-113">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="4c2f0-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4c2f0-114">Return code</span></span>                                                                          | <span data-ttu-id="4c2f0-115">Description</span><span class="sxs-lookup"><span data-stu-id="4c2f0-115">Description</span></span>                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c2f0-116"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="4c2f0-116"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="4c2f0-117">複製檔案並覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-117">Copy the file and overwrite the existing file.</span></span><br/>               |
| <dl> <span data-ttu-id="4c2f0-118"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="4c2f0-118"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="4c2f0-119">略過複製操作。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-119">Skip the copy operation.</span></span> <span data-ttu-id="4c2f0-120">請勿覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-120">Do not overwrite the existing file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4c2f0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c2f0-121">Requirements</span></span>



| <span data-ttu-id="4c2f0-122">需求</span><span class="sxs-lookup"><span data-stu-id="4c2f0-122">Requirement</span></span> | <span data-ttu-id="4c2f0-123">值</span><span class="sxs-lookup"><span data-stu-id="4c2f0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2f0-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c2f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4c2f0-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c2f0-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4c2f0-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c2f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4c2f0-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c2f0-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c2f0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4c2f0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c2f0-129"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c2f0-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c2f0-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c2f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c2f0-131">概觀</span><span class="sxs-lookup"><span data-stu-id="4c2f0-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="4c2f0-132">通知</span><span class="sxs-lookup"><span data-stu-id="4c2f0-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="4c2f0-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="4c2f0-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="4c2f0-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="4c2f0-136">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-136">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="4c2f0-137">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-137">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="4c2f0-138">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-138">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




