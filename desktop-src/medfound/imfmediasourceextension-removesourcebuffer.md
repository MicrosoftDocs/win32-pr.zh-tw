---
description: 從 IMFMediaSourceExtension 物件所管理的來源緩衝區集合中移除指定的來源緩衝區。
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: IMFMediaSourceExtension：： RemoveSourceBuffer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321583"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a><span data-ttu-id="0090c-103">IMFMediaSourceExtension：： RemoveSourceBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="0090c-103">IMFMediaSourceExtension::RemoveSourceBuffer method</span></span>

<span data-ttu-id="0090c-104">從 [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) 物件所管理的來源緩衝區集合中移除指定的來源緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0090c-104">Removes the specified source buffer from the collection of source buffers managed by the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0090c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0090c-105">Syntax</span></span>


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0090c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0090c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0090c-107">*pSourceBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0090c-107">*pSourceBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0090c-108">要移除的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0090c-108">The buffer to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0090c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0090c-109">Return value</span></span>

<span data-ttu-id="0090c-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0090c-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0090c-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0090c-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0090c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0090c-112">Requirements</span></span>



| <span data-ttu-id="0090c-113">需求</span><span class="sxs-lookup"><span data-stu-id="0090c-113">Requirement</span></span> | <span data-ttu-id="0090c-114">值</span><span class="sxs-lookup"><span data-stu-id="0090c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0090c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0090c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0090c-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0090c-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0090c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0090c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0090c-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0090c-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0090c-119">Idl</span><span class="sxs-lookup"><span data-stu-id="0090c-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0090c-120"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0090c-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0090c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0090c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0090c-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="0090c-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




