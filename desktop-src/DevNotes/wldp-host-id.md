---
description: 識別 WLDP 呼叫端的主機類型。
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: 'WLDP_HOST_ID 列舉 (Wldp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510392"
---
# <a name="wldp_host_id-enumeration"></a><span data-ttu-id="fffe1-103">WLDP \_ 主機 \_ 識別碼列舉</span><span class="sxs-lookup"><span data-stu-id="fffe1-103">WLDP\_HOST\_ID enumeration</span></span>

<span data-ttu-id="fffe1-104">識別 WLDP 呼叫端的主機類型。</span><span class="sxs-lookup"><span data-stu-id="fffe1-104">Identifies the host type of the WLDP caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffe1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fffe1-105">Syntax</span></span>


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a><span data-ttu-id="fffe1-106">常數</span><span class="sxs-lookup"><span data-stu-id="fffe1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fffe1-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_主機 \_ 識別碼 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="fffe1-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span> **WLDP\_HOST\_ID\_UNKNOWN**</span></span> 
</dt> <dd>

<span data-ttu-id="fffe1-108">主機類型未知。</span><span class="sxs-lookup"><span data-stu-id="fffe1-108">The host type is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="fffe1-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_主機 \_ 識別碼 \_ 全域**</span><span class="sxs-lookup"><span data-stu-id="fffe1-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span> **WLDP\_HOST\_ID\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="fffe1-110">主機類型為全域原則。</span><span class="sxs-lookup"><span data-stu-id="fffe1-110">The host type is global policy.</span></span>

</dd> <dt>

<span data-ttu-id="fffe1-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP \_ 主機 \_ 識別碼 \_ VBA**</span><span class="sxs-lookup"><span data-stu-id="fffe1-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP\_HOST\_ID\_VBA**</span></span>
</dt> <dd>

<span data-ttu-id="fffe1-112">主機類型為 VBScript。</span><span class="sxs-lookup"><span data-stu-id="fffe1-112">The host type is VBScript.</span></span>

</dd> <dt>

<span data-ttu-id="fffe1-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_主機 \_ 識別碼 \_ WSH**</span><span class="sxs-lookup"><span data-stu-id="fffe1-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span> **WLDP\_HOST\_ID\_WSH**</span></span>
</dt> <dd>

<span data-ttu-id="fffe1-114">主機類型為 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="fffe1-114">The host type is Windows Script Host.</span></span>

</dd> <dt>

<span data-ttu-id="fffe1-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_主機 \_ 識別碼 \_ POWERSHELL**</span><span class="sxs-lookup"><span data-stu-id="fffe1-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span> **WLDP\_HOST\_ID\_POWERSHELL**</span></span>
</dt> <dd>

<span data-ttu-id="fffe1-116">主機類型為 Windows Powershell。</span><span class="sxs-lookup"><span data-stu-id="fffe1-116">The host type is Windows Powershell.</span></span>

</dd> <dt>

<span data-ttu-id="fffe1-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_主機 \_ 識別碼 \_ IE**</span><span class="sxs-lookup"><span data-stu-id="fffe1-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span> **WLDP\_HOST\_ID\_IE**</span></span>
</dt> <dd>

<span data-ttu-id="fffe1-118">主機類型為 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="fffe1-118">The host type is Internet Explorer.</span></span>

</dd> <dt>

<span data-ttu-id="fffe1-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_主機 \_ 識別碼 \_ MSI**</span><span class="sxs-lookup"><span data-stu-id="fffe1-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span> **WLDP\_HOST\_ID\_MSI**</span></span>
</dt> <dd>

<span data-ttu-id="fffe1-120">主機類型為 Microsoft Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="fffe1-120">The host type is the Microsoft Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="fffe1-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_主機 \_ 識別碼 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="fffe1-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span> **WLDP\_HOST\_ID\_MAX**</span></span> 
</dt> <dd>

<span data-ttu-id="fffe1-122">最大的列舉值。</span><span class="sxs-lookup"><span data-stu-id="fffe1-122">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fffe1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fffe1-123">Requirements</span></span>



| <span data-ttu-id="fffe1-124">需求</span><span class="sxs-lookup"><span data-stu-id="fffe1-124">Requirement</span></span> | <span data-ttu-id="fffe1-125">值</span><span class="sxs-lookup"><span data-stu-id="fffe1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fffe1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fffe1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fffe1-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fffe1-127">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fffe1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fffe1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fffe1-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fffe1-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fffe1-130">標頭</span><span class="sxs-lookup"><span data-stu-id="fffe1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fffe1-131"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fffe1-131"><dt>Wldp.h</dt></span></span> </dl> |



 

 




