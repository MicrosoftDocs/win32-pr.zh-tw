---
title: IMsRdpClientAdvancedSettings SasSequence 屬性
description: 指定用戶端將用來存取伺服器上登入畫面 (SAS) 的安全存取順序。
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- SasSequence 屬性遠端桌面服務
- SasSequence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，SasSequence 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464320"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a><span data-ttu-id="0a465-106">IMsRdpClientAdvancedSettings：： SasSequence 屬性</span><span class="sxs-lookup"><span data-stu-id="0a465-106">IMsRdpClientAdvancedSettings::SasSequence property</span></span>

<span data-ttu-id="0a465-107">指定用戶端將用來存取伺服器上登入畫面 (SAS) 的安全存取順序。</span><span class="sxs-lookup"><span data-stu-id="0a465-107">Specifies the secure access sequence (SAS) the client will use to access the login screen on the server.</span></span>

<span data-ttu-id="0a465-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0a465-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a465-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a465-109">Syntax</span></span>


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a><span data-ttu-id="0a465-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="0a465-110">Property value</span></span>

<span data-ttu-id="0a465-111">包含 SAS 指標的 **長** 數值。</span><span class="sxs-lookup"><span data-stu-id="0a465-111">A **LONG** value that contains the SAS indicator.</span></span> <span data-ttu-id="0a465-112">唯一支援的值是0xaa03，表示標準 CTRL + ALT + DELETE 序列。</span><span class="sxs-lookup"><span data-stu-id="0a465-112">The only supported value is 0xaa03, which indicates the standard CTRL+ALT+DELETE sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a465-113">備註</span><span class="sxs-lookup"><span data-stu-id="0a465-113">Remarks</span></span>

<span data-ttu-id="0a465-114">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="0a465-114">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a465-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a465-115">Requirements</span></span>



| <span data-ttu-id="0a465-116">需求</span><span class="sxs-lookup"><span data-stu-id="0a465-116">Requirement</span></span> | <span data-ttu-id="0a465-117">值</span><span class="sxs-lookup"><span data-stu-id="0a465-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a465-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a465-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a465-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a465-119">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0a465-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a465-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a465-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a465-121">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0a465-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0a465-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a465-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a465-123"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0a465-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0a465-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a465-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a465-125"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0a465-126">IID</span><span class="sxs-lookup"><span data-stu-id="0a465-126">IID</span></span><br/>                      | <span data-ttu-id="0a465-127">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0a465-127">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a465-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a465-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a465-129">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0a465-129">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





