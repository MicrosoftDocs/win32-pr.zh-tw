---
description: 包含 EAPOL 設定參數。
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: 'EAPOL_INTF_PARAMS 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984557"
---
# <a name="eapol_intf_params-structure"></a><span data-ttu-id="498b8-103">EAPOL \_ INTF \_ PARAMS 結構</span><span class="sxs-lookup"><span data-stu-id="498b8-103">EAPOL\_INTF\_PARAMS structure</span></span>

<span data-ttu-id="498b8-104">\[**EAPOL \_Windows \_** Vista 和 windows Server 2008 已不再支援 INTF 參數。</span><span class="sxs-lookup"><span data-stu-id="498b8-104">\[**EAPOL\_INTF\_PARAMS** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="498b8-105">相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="498b8-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="498b8-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="498b8-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="498b8-107">包含 EAPOL 設定參數。</span><span class="sxs-lookup"><span data-stu-id="498b8-107">Contains EAPOL configuration parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="498b8-108">語法</span><span class="sxs-lookup"><span data-stu-id="498b8-108">Syntax</span></span>


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a><span data-ttu-id="498b8-109">成員</span><span class="sxs-lookup"><span data-stu-id="498b8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="498b8-110">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="498b8-110">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="498b8-111">呼叫端的版本。</span><span class="sxs-lookup"><span data-stu-id="498b8-111">Version of the caller.</span></span> <span data-ttu-id="498b8-112">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="498b8-112">Default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="498b8-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="498b8-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="498b8-114">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="498b8-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="498b8-115">**dwEapFlags**</span><span class="sxs-lookup"><span data-stu-id="498b8-115">**dwEapFlags**</span></span>
</dt> <dd>

<span data-ttu-id="498b8-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="498b8-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="498b8-117">**dwEapType**</span><span class="sxs-lookup"><span data-stu-id="498b8-117">**dwEapType**</span></span>
</dt> <dd>

<span data-ttu-id="498b8-118">要使用的 EAP 延伸模組類型。</span><span class="sxs-lookup"><span data-stu-id="498b8-118">The EAP extension type to be used.</span></span> <span data-ttu-id="498b8-119">針對 EAP-TLS，將0x00000026 設為0x00000013，並針對 PEAP 設定為。</span><span class="sxs-lookup"><span data-stu-id="498b8-119">Set to 0x00000013 for EAP-TLS and 0x00000026 for PEAP.</span></span>

</dd> <dt>

<span data-ttu-id="498b8-120">**dwSizeOfSSID**</span><span class="sxs-lookup"><span data-stu-id="498b8-120">**dwSizeOfSSID**</span></span>
</dt> <dd>

<span data-ttu-id="498b8-121">網路識別碼的大小。</span><span class="sxs-lookup"><span data-stu-id="498b8-121">Size of network identifier.</span></span>

</dd> <dt>

<span data-ttu-id="498b8-122">**bSSID**</span><span class="sxs-lookup"><span data-stu-id="498b8-122">**bSSID**</span></span>
</dt> <dd>

<span data-ttu-id="498b8-123">網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="498b8-123">Network identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="498b8-124">備註</span><span class="sxs-lookup"><span data-stu-id="498b8-124">Remarks</span></span>

<span data-ttu-id="498b8-125">Windows SDK 不提供標頭檔 wzcsapi。</span><span class="sxs-lookup"><span data-stu-id="498b8-125">The header file wzcsapi.h is not available in the Windows SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="498b8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="498b8-126">Requirements</span></span>



| <span data-ttu-id="498b8-127">需求</span><span class="sxs-lookup"><span data-stu-id="498b8-127">Requirement</span></span> | <span data-ttu-id="498b8-128">值</span><span class="sxs-lookup"><span data-stu-id="498b8-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="498b8-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="498b8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="498b8-130">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="498b8-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="498b8-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="498b8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="498b8-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="498b8-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="498b8-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="498b8-133">End of client support</span></span><br/>    | <span data-ttu-id="498b8-134">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="498b8-134">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="498b8-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="498b8-135">End of server support</span></span><br/>    | <span data-ttu-id="498b8-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="498b8-136">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="498b8-137">標頭</span><span class="sxs-lookup"><span data-stu-id="498b8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="498b8-138"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="498b8-138"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




