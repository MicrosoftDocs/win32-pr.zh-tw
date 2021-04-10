---
title: IRemoteDesktopClient 設定屬性
description: 抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的設定物件。
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Settings 屬性遠端桌面服務
- Settings 屬性遠端桌面服務，IRemoteDesktopClient 介面
- IRemoteDesktopClient 介面遠端桌面服務，Settings 屬性
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934660"
---
# <a name="iremotedesktopclientsettings-property"></a><span data-ttu-id="73a0b-106">IRemoteDesktopClient：： Settings 屬性</span><span class="sxs-lookup"><span data-stu-id="73a0b-106">IRemoteDesktopClient::Settings property</span></span>

<span data-ttu-id="73a0b-107">抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的設定物件。</span><span class="sxs-lookup"><span data-stu-id="73a0b-107">Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.</span></span>

<span data-ttu-id="73a0b-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="73a0b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a0b-109">語法</span><span class="sxs-lookup"><span data-stu-id="73a0b-109">Syntax</span></span>


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a><span data-ttu-id="73a0b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="73a0b-110">Property value</span></span>

<span data-ttu-id="73a0b-111">RDP 用戶端的設定物件。</span><span class="sxs-lookup"><span data-stu-id="73a0b-111">The settings object for the RDP client.</span></span>

## <a name="requirements"></a><span data-ttu-id="73a0b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="73a0b-112">Requirements</span></span>



| <span data-ttu-id="73a0b-113">需求</span><span class="sxs-lookup"><span data-stu-id="73a0b-113">Requirement</span></span> | <span data-ttu-id="73a0b-114">值</span><span class="sxs-lookup"><span data-stu-id="73a0b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73a0b-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73a0b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="73a0b-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="73a0b-116">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="73a0b-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73a0b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="73a0b-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73a0b-118">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="73a0b-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="73a0b-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="73a0b-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73a0b-120"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="73a0b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="73a0b-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73a0b-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73a0b-122"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="73a0b-123">IID</span><span class="sxs-lookup"><span data-stu-id="73a0b-123">IID</span></span><br/>                      | <span data-ttu-id="73a0b-124">IID \_ IRemoteDesktopClient 定義為 57D25668-625A-4905-BE4E-304CAA13F89C</span><span class="sxs-lookup"><span data-stu-id="73a0b-124">IID\_IRemoteDesktopClient is defined as 57D25668-625A-4905-BE4E-304CAA13F89C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73a0b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73a0b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a0b-126">**IRemoteDesktopClient**</span><span class="sxs-lookup"><span data-stu-id="73a0b-126">**IRemoteDesktopClient**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

