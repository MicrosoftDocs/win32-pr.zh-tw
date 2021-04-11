---
title: 'MP_FASTPATH_TYPE 列舉 (MpClient .h) '
description: FastPath 類型。
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE 列舉舊版 Windows 環境功能
- PMP_FASTPATH_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105779"
---
# <a name="mp_fastpath_type-enumeration"></a><span data-ttu-id="ec87e-105">MP \_ FASTPATH \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="ec87e-105">MP\_FASTPATH\_TYPE enumeration</span></span>

<span data-ttu-id="ec87e-106">FastPath 類型。</span><span class="sxs-lookup"><span data-stu-id="ec87e-106">FastPath type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec87e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec87e-107">Syntax</span></span>


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ec87e-108">常數</span><span class="sxs-lookup"><span data-stu-id="ec87e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ec87e-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP \_ FASTPATH \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="ec87e-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP\_FASTPATH\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ec87e-110">不明。</span><span class="sxs-lookup"><span data-stu-id="ec87e-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="ec87e-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP \_ FASTPATH \_ VDM**</span><span class="sxs-lookup"><span data-stu-id="ec87e-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP\_FASTPATH\_VDM**</span></span>
</dt> <dd>

<span data-ttu-id="ec87e-112">VDM 更新。</span><span class="sxs-lookup"><span data-stu-id="ec87e-112">VDM update.</span></span>

</dd> <dt>

<span data-ttu-id="ec87e-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP \_ FASTPATH \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="ec87e-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP\_FASTPATH\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="ec87e-114">簽章停用通知。</span><span class="sxs-lookup"><span data-stu-id="ec87e-114">Signature disable notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec87e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec87e-115">Requirements</span></span>



| <span data-ttu-id="ec87e-116">需求</span><span class="sxs-lookup"><span data-stu-id="ec87e-116">Requirement</span></span> | <span data-ttu-id="ec87e-117">值</span><span class="sxs-lookup"><span data-stu-id="ec87e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec87e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec87e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec87e-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec87e-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ec87e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec87e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec87e-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec87e-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec87e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ec87e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec87e-123"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec87e-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





