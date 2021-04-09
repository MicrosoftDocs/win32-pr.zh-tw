---
description: 指出暫止進程正在啟動，而且資源應該會進入一致的狀態。
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: IMFCdmSuspendNotify：： Begin 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689508"
---
# <a name="imfcdmsuspendnotifybegin-method"></a><span data-ttu-id="3ace2-103">IMFCdmSuspendNotify：： Begin 方法</span><span class="sxs-lookup"><span data-stu-id="3ace2-103">IMFCdmSuspendNotify::Begin method</span></span>

<span data-ttu-id="3ace2-104">指出暫止進程正在啟動，而且資源應該會進入一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ace2-104">Indicates that the suspend process is starting and resources should be brought into a consistent state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ace2-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ace2-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="3ace2-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ace2-106">Parameters</span></span>

<span data-ttu-id="3ace2-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3ace2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ace2-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ace2-108">Return value</span></span>

<span data-ttu-id="3ace2-109">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3ace2-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ace2-110">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3ace2-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ace2-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ace2-111">Requirements</span></span>



| <span data-ttu-id="3ace2-112">需求</span><span class="sxs-lookup"><span data-stu-id="3ace2-112">Requirement</span></span> | <span data-ttu-id="3ace2-113">值</span><span class="sxs-lookup"><span data-stu-id="3ace2-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ace2-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ace2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3ace2-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ace2-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3ace2-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ace2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3ace2-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ace2-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3ace2-118">Idl</span><span class="sxs-lookup"><span data-stu-id="3ace2-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ace2-119"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ace2-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ace2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ace2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ace2-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="3ace2-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




