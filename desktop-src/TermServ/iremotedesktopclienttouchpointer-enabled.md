---
title: IRemoteDesktopClientTouchPointer Enabled 屬性
description: RDP 應用程式容器用戶端控制項上是否啟用觸控指標功能。
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Enabled 屬性遠端桌面服務
- Enabled 屬性遠端桌面服務，IRemoteDesktopClientTouchPointer 介面
- IRemoteDesktopClientTouchPointer 介面遠端桌面服務，Enabled 屬性
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969793"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a><span data-ttu-id="2f385-106">IRemoteDesktopClientTouchPointer：： Enabled 屬性</span><span class="sxs-lookup"><span data-stu-id="2f385-106">IRemoteDesktopClientTouchPointer::Enabled property</span></span>

<span data-ttu-id="2f385-107">RDP 應用程式容器用戶端控制項上是否啟用觸控指標功能。</span><span class="sxs-lookup"><span data-stu-id="2f385-107">Whether the touch pointer feature is enabled on the RDP app container client control.</span></span>

<span data-ttu-id="2f385-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f385-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f385-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f385-109">Syntax</span></span>


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="2f385-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2f385-110">Property value</span></span>

<span data-ttu-id="2f385-111">如果已啟用觸控指標功能，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="2f385-111">**true** if the touch pointer feature is enabled; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f385-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f385-112">Requirements</span></span>



| <span data-ttu-id="2f385-113">需求</span><span class="sxs-lookup"><span data-stu-id="2f385-113">Requirement</span></span> | <span data-ttu-id="2f385-114">值</span><span class="sxs-lookup"><span data-stu-id="2f385-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f385-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f385-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2f385-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f385-116">Windows 8</span></span><br/>                                                                                |
| <span data-ttu-id="2f385-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f385-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2f385-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f385-118">Windows Server 2012</span></span><br/>                                                                      |
| <span data-ttu-id="2f385-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2f385-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f385-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f385-120"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="2f385-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2f385-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f385-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f385-122"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="2f385-123">IID</span><span class="sxs-lookup"><span data-stu-id="2f385-123">IID</span></span><br/>                      | <span data-ttu-id="2f385-124">IID \_ IRemoteDesktopClientTouchPointer 定義為260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span><span class="sxs-lookup"><span data-stu-id="2f385-124">IID\_IRemoteDesktopClientTouchPointer is defined as 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f385-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f385-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f385-126">**IRemoteDesktopClientTouchPointer**</span><span class="sxs-lookup"><span data-stu-id="2f385-126">**IRemoteDesktopClientTouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

