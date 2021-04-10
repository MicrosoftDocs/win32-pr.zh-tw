---
title: IMsRdpClientAdvancedSettings8 ClientProtocolSpec 屬性
description: 指定用戶端與伺服器之間使用的遠端桌面通訊協定。
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- ClientProtocolSpec 屬性遠端桌面服務
- ClientProtocolSpec 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ClientProtocolSpec 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e603f7587435b3701ec0511587286e1a38bcc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934061"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a><span data-ttu-id="cad9f-106">IMsRdpClientAdvancedSettings8：： ClientProtocolSpec 屬性</span><span class="sxs-lookup"><span data-stu-id="cad9f-106">IMsRdpClientAdvancedSettings8::ClientProtocolSpec property</span></span>

<span data-ttu-id="cad9f-107">指定用戶端與伺服器之間使用的遠端桌面通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cad9f-107">Specifies the remote desktop protocol used between the client and the server.</span></span>

<span data-ttu-id="cad9f-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cad9f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad9f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad9f-109">Syntax</span></span>


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a><span data-ttu-id="cad9f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="cad9f-110">Property value</span></span>

<span data-ttu-id="cad9f-111">[**ClientSpec**](clientspec.md)列舉的值，指定用戶端與伺服器之間使用的遠端桌面通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cad9f-111">A value of the [**ClientSpec**](clientspec.md) enumeration that specifies the remote desktop protocol used between the client and the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad9f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cad9f-112">Requirements</span></span>



| <span data-ttu-id="cad9f-113">需求</span><span class="sxs-lookup"><span data-stu-id="cad9f-113">Requirement</span></span> | <span data-ttu-id="cad9f-114">值</span><span class="sxs-lookup"><span data-stu-id="cad9f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cad9f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cad9f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cad9f-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cad9f-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="cad9f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cad9f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cad9f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cad9f-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="cad9f-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="cad9f-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="cad9f-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cad9f-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cad9f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cad9f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cad9f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cad9f-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad9f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cad9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad9f-124">**ClientSpec**</span><span class="sxs-lookup"><span data-stu-id="cad9f-124">**ClientSpec**</span></span>](clientspec.md)
</dt> <dt>

[<span data-ttu-id="cad9f-125">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="cad9f-125">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





