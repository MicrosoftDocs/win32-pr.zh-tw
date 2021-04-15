---
title: 'MP_SIGNATURE_TYPE 列舉 (MpClient .h) '
description: 可能的簽章類型。
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE 列舉舊版 Windows 環境功能
- PMP_SIGNATURE_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465165"
---
# <a name="mp_signature_type-enumeration"></a><span data-ttu-id="ed7fb-105">MP \_ SIGNATURE \_ TYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="ed7fb-105">MP\_SIGNATURE\_TYPE enumeration</span></span>

<span data-ttu-id="ed7fb-106">可能的簽章類型。</span><span class="sxs-lookup"><span data-stu-id="ed7fb-106">Possible signature types.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed7fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed7fb-107">Syntax</span></span>


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ed7fb-108">常數</span><span class="sxs-lookup"><span data-stu-id="ed7fb-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed7fb-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP \_ SIGNATURE \_ 反惡意程式碼**</span><span class="sxs-lookup"><span data-stu-id="ed7fb-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP\_SIGNATURE\_ANTIMALWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ed7fb-110">防毒軟體和反間諜軟體簽章。</span><span class="sxs-lookup"><span data-stu-id="ed7fb-110">Both antivirus and antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ed7fb-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP \_ SIGNATURE \_ 防毒軟體**</span><span class="sxs-lookup"><span data-stu-id="ed7fb-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP\_SIGNATURE\_ANTIVIRUS**</span></span>
</dt> <dd>

<span data-ttu-id="ed7fb-112">僅限防毒軟體簽章。</span><span class="sxs-lookup"><span data-stu-id="ed7fb-112">Only antivirus signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ed7fb-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP \_ 簽名 \_ 反間諜軟體**</span><span class="sxs-lookup"><span data-stu-id="ed7fb-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP\_SIGNATURE\_ANTISPYWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ed7fb-114">只有反間諜軟體簽章。</span><span class="sxs-lookup"><span data-stu-id="ed7fb-114">Only antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ed7fb-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP \_ SIGNATURE \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="ed7fb-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP\_SIGNATURE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="ed7fb-116">NIS 簽章。</span><span class="sxs-lookup"><span data-stu-id="ed7fb-116">NIS signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ed7fb-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP \_ SIGNATURE \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="ed7fb-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP\_SIGNATURE\_TYPES\_MAXVALUE**</span></span>
<span data-ttu-id="ed7fb-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ed7fb-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ed7fb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed7fb-119">Requirements</span></span>



| <span data-ttu-id="ed7fb-120">需求</span><span class="sxs-lookup"><span data-stu-id="ed7fb-120">Requirement</span></span> | <span data-ttu-id="ed7fb-121">值</span><span class="sxs-lookup"><span data-stu-id="ed7fb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7fb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed7fb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed7fb-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed7fb-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ed7fb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed7fb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed7fb-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed7fb-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed7fb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ed7fb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed7fb-127"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed7fb-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





