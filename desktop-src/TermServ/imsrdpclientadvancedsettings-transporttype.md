---
title: IMsRdpClientAdvancedSettings TransportType 屬性
description: 指定用戶端所使用的傳輸類型。
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- TransportType 屬性遠端桌面服務
- TransportType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，TransportType 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968739"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a><span data-ttu-id="a466c-106">IMsRdpClientAdvancedSettings：： TransportType 屬性</span><span class="sxs-lookup"><span data-stu-id="a466c-106">IMsRdpClientAdvancedSettings::TransportType property</span></span>

<span data-ttu-id="a466c-107">指定用戶端所使用的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="a466c-107">Specifies the transport type used by the client.</span></span> <span data-ttu-id="a466c-108">遠端桌面 ActiveX 控制項不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a466c-108">This property is not used by the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="a466c-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a466c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a466c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a466c-110">Syntax</span></span>


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a><span data-ttu-id="a466c-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="a466c-111">Property value</span></span>

<span data-ttu-id="a466c-112">設定傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="a466c-112">Sets the transport type.</span></span> <span data-ttu-id="a466c-113">這個方法可能會成功，但是遠端桌面 ActiveX 控制項絕不會使用設定的值。</span><span class="sxs-lookup"><span data-stu-id="a466c-113">This method may succeed, but the value set is never used by the Remote Desktop ActiveX control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a466c-114">備註</span><span class="sxs-lookup"><span data-stu-id="a466c-114">Remarks</span></span>

<span data-ttu-id="a466c-115">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="a466c-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a466c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a466c-116">Requirements</span></span>



| <span data-ttu-id="a466c-117">需求</span><span class="sxs-lookup"><span data-stu-id="a466c-117">Requirement</span></span> | <span data-ttu-id="a466c-118">值</span><span class="sxs-lookup"><span data-stu-id="a466c-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a466c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a466c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a466c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a466c-120">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a466c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a466c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a466c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a466c-122">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a466c-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a466c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="a466c-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-124"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a466c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a466c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a466c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-126"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a466c-127">IID</span><span class="sxs-lookup"><span data-stu-id="a466c-127">IID</span></span><br/>                      | <span data-ttu-id="a466c-128">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a466c-128">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a466c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a466c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a466c-130">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a466c-130">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





