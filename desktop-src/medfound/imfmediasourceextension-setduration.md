---
description: 設定媒體來源的持續時間（100-毫微秒單位）。
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: IMFMediaSourceExtension：： SetDuration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974766"
---
# <a name="imfmediasourceextensionsetduration-method"></a><span data-ttu-id="ee212-103">IMFMediaSourceExtension：： SetDuration 方法</span><span class="sxs-lookup"><span data-stu-id="ee212-103">IMFMediaSourceExtension::SetDuration method</span></span>

<span data-ttu-id="ee212-104">設定媒體來源的持續時間（100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="ee212-104">Sets the duration of the media source in 100-nanosecond units.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee212-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee212-105">Syntax</span></span>


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a><span data-ttu-id="ee212-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee212-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee212-107">*持續時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee212-107">*duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee212-108">媒體來源的持續時間（100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="ee212-108">The duration of the media source in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee212-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee212-109">Return value</span></span>

<span data-ttu-id="ee212-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ee212-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee212-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee212-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee212-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee212-112">Requirements</span></span>



| <span data-ttu-id="ee212-113">需求</span><span class="sxs-lookup"><span data-stu-id="ee212-113">Requirement</span></span> | <span data-ttu-id="ee212-114">值</span><span class="sxs-lookup"><span data-stu-id="ee212-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee212-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee212-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee212-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee212-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ee212-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee212-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee212-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee212-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ee212-119">Idl</span><span class="sxs-lookup"><span data-stu-id="ee212-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee212-120"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee212-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee212-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee212-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee212-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="ee212-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




