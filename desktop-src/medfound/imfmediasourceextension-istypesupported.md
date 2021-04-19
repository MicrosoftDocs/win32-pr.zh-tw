---
description: 取得值，這個值會指出媒體來源是否支援指定的 MIME 類型。
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: IMFMediaSourceExtension：： IsTypeSupported 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106991395"
---
# <a name="imfmediasourceextensionistypesupported-method"></a><span data-ttu-id="ccc14-103">IMFMediaSourceExtension：： IsTypeSupported 方法</span><span class="sxs-lookup"><span data-stu-id="ccc14-103">IMFMediaSourceExtension::IsTypeSupported method</span></span>

<span data-ttu-id="ccc14-104">取得值，這個值會指出媒體來源是否支援指定的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="ccc14-104">Gets a value that indicates if the specified MIME type is supported by the media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc14-105">語法</span><span class="sxs-lookup"><span data-stu-id="ccc14-105">Syntax</span></span>


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a><span data-ttu-id="ccc14-106">參數</span><span class="sxs-lookup"><span data-stu-id="ccc14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc14-107">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc14-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc14-108">要檢查支援的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ccc14-108">The media type to check support for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc14-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccc14-109">Return value</span></span>

<span data-ttu-id="ccc14-110">如果支援媒體類型，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="ccc14-110">**true** if the media type is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc14-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccc14-111">Requirements</span></span>



| <span data-ttu-id="ccc14-112">需求</span><span class="sxs-lookup"><span data-stu-id="ccc14-112">Requirement</span></span> | <span data-ttu-id="ccc14-113">值</span><span class="sxs-lookup"><span data-stu-id="ccc14-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc14-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccc14-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc14-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccc14-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ccc14-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccc14-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc14-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccc14-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ccc14-118">Idl</span><span class="sxs-lookup"><span data-stu-id="ccc14-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ccc14-119"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ccc14-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc14-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccc14-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc14-121">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="ccc14-121">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




