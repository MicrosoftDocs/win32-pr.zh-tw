---
description: 將指定的媒體區段附加至 IMFSourceBuffer。
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: IMFSourceBuffer：： Append 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191634"
---
# <a name="imfsourcebufferappend-method"></a><span data-ttu-id="06035-103">IMFSourceBuffer：： Append 方法</span><span class="sxs-lookup"><span data-stu-id="06035-103">IMFSourceBuffer::Append method</span></span>

<span data-ttu-id="06035-104">將指定的媒體區段附加至 [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)。</span><span class="sxs-lookup"><span data-stu-id="06035-104">Appends the specified media segment to the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="06035-105">語法</span><span class="sxs-lookup"><span data-stu-id="06035-105">Syntax</span></span>


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a><span data-ttu-id="06035-106">參數</span><span class="sxs-lookup"><span data-stu-id="06035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06035-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06035-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06035-108">要附加的媒體資料。</span><span class="sxs-lookup"><span data-stu-id="06035-108">The media data to append.</span></span>

</dd> <dt>

<span data-ttu-id="06035-109">*len* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06035-109">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06035-110">儲存在 *.pdata* 中的媒體資料長度。</span><span class="sxs-lookup"><span data-stu-id="06035-110">The length of the media data stored in *pData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06035-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="06035-111">Return value</span></span>

<span data-ttu-id="06035-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="06035-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06035-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06035-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06035-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="06035-114">Requirements</span></span>



| <span data-ttu-id="06035-115">需求</span><span class="sxs-lookup"><span data-stu-id="06035-115">Requirement</span></span> | <span data-ttu-id="06035-116">值</span><span class="sxs-lookup"><span data-stu-id="06035-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06035-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06035-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06035-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06035-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="06035-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06035-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06035-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06035-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="06035-121">Idl</span><span class="sxs-lookup"><span data-stu-id="06035-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06035-122"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="06035-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06035-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06035-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06035-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="06035-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




