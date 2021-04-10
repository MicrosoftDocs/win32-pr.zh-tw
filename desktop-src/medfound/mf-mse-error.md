---
description: 定義媒體來源延伸模組的不同錯誤狀態。
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: MF_MSE_ERROR 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114601"
---
# <a name="mf_mse_error-enumeration"></a><span data-ttu-id="b97fc-103">MF \_ MSE \_ 錯誤列舉</span><span class="sxs-lookup"><span data-stu-id="b97fc-103">MF\_MSE\_ERROR enumeration</span></span>

<span data-ttu-id="b97fc-104">定義媒體來源延伸模組的不同錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="b97fc-104">Defines the different error states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b97fc-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a><span data-ttu-id="b97fc-106">常數</span><span class="sxs-lookup"><span data-stu-id="b97fc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b97fc-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF \_ MSE \_ 錯誤 \_ >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR**</span><span class="sxs-lookup"><span data-stu-id="b97fc-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF\_MSE\_ERROR\_NOERROR**</span></span>
</dt> <dd>

<span data-ttu-id="b97fc-108">未指定錯誤。</span><span class="sxs-lookup"><span data-stu-id="b97fc-108">Specifies no error.</span></span>

</dd> <dt>

<span data-ttu-id="b97fc-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF \_ MSE \_ 錯誤 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="b97fc-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF\_MSE\_ERROR\_NETWORK**</span></span>
</dt> <dd>

<span data-ttu-id="b97fc-110">指定網路發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b97fc-110">Specifies an error with the network.</span></span>

</dd> <dt>

<span data-ttu-id="b97fc-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF \_ MSE \_ 錯誤 \_ 解碼**</span><span class="sxs-lookup"><span data-stu-id="b97fc-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF\_MSE\_ERROR\_DECODE**</span></span>
</dt> <dd>

<span data-ttu-id="b97fc-112">指定解碼時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b97fc-112">Specifies an error with decoding.</span></span>

</dd> <dt>

<span data-ttu-id="b97fc-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF \_ MSE \_ 錯誤 \_ 不明 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="b97fc-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF\_MSE\_ERROR\_UNKNOWN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="b97fc-114">指定未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b97fc-114">Specifies an unknown error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b97fc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b97fc-115">Requirements</span></span>



| <span data-ttu-id="b97fc-116">需求</span><span class="sxs-lookup"><span data-stu-id="b97fc-116">Requirement</span></span> | <span data-ttu-id="b97fc-117">值</span><span class="sxs-lookup"><span data-stu-id="b97fc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b97fc-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b97fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b97fc-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b97fc-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b97fc-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b97fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b97fc-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b97fc-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b97fc-122">Idl</span><span class="sxs-lookup"><span data-stu-id="b97fc-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b97fc-123"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b97fc-123"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b97fc-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b97fc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97fc-125">媒體基礎列舉</span><span class="sxs-lookup"><span data-stu-id="b97fc-125">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




