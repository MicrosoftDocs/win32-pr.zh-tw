---
title: IMsRdpExtendedSettings 屬性屬性
description: 包含已命名的屬性。
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Property 屬性遠端桌面服務
- Property 屬性遠端桌面服務，IMsRdpExtendedSettings 介面
- IMsRdpExtendedSettings 介面遠端桌面服務，Property 屬性
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "103687352"
---
# <a name="imsrdpextendedsettingsproperty-property"></a><span data-ttu-id="9d24a-106">IMsRdpExtendedSettings：:P roperty 屬性</span><span class="sxs-lookup"><span data-stu-id="9d24a-106">IMsRdpExtendedSettings::Property property</span></span>

<span data-ttu-id="9d24a-107">包含已命名的屬性。</span><span class="sxs-lookup"><span data-stu-id="9d24a-107">Contains a named property.</span></span>

<span data-ttu-id="9d24a-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9d24a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d24a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d24a-109">Syntax</span></span>


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a><span data-ttu-id="9d24a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9d24a-110">Property value</span></span>

<span data-ttu-id="9d24a-111">已命名的屬性值。</span><span class="sxs-lookup"><span data-stu-id="9d24a-111">The named property value.</span></span>

| <span data-ttu-id="9d24a-112">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="9d24a-112">Property name</span></span> | <span data-ttu-id="9d24a-113">資料類型</span><span class="sxs-lookup"><span data-stu-id="9d24a-113">Data type</span></span> | <span data-ttu-id="9d24a-114">Access</span><span class="sxs-lookup"><span data-stu-id="9d24a-114">Access</span></span> | <span data-ttu-id="9d24a-115">可以在連接開始之後變更</span><span class="sxs-lookup"><span data-stu-id="9d24a-115">Can be changed after connection started</span></span> | <span data-ttu-id="9d24a-116">Description</span><span class="sxs-lookup"><span data-stu-id="9d24a-116">Description</span></span> |
|----------|-----------|--------|-----------------------------------------|-------------|
| <span data-ttu-id="9d24a-117">ConnectToChildSession</span><span class="sxs-lookup"><span data-stu-id="9d24a-117">ConnectToChildSession</span></span> | <span data-ttu-id="9d24a-118">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="9d24a-118">**VT\_BOOL**</span></span> | <span data-ttu-id="9d24a-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d24a-119">Read/Write</span></span> | <span data-ttu-id="9d24a-120">Yes</span><span class="sxs-lookup"><span data-stu-id="9d24a-120">Yes</span></span> | <span data-ttu-id="9d24a-121">將這個屬性設定為 **True** ，會導致用戶端控制項連接到本機電腦上的子會話，而不是遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="9d24a-121">Setting this property to **True** causes the client control to connect to the child session on the local machine instead of a remote server.</span></span> <span data-ttu-id="9d24a-122">如果這個屬性設定為 **true**，您就無法連接到遠端伺服器，因為所有連接都會重新導向至 localhost。</span><span class="sxs-lookup"><span data-stu-id="9d24a-122">If this property is set to **true**, you cannot connect to a remote server because all connections are redirected to localhost.</span></span> <span data-ttu-id="9d24a-123">如需子會話的詳細資訊，請參閱 [子會話](child-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="9d24a-123">For more information about child sessions, see [Child Sessions](child-sessions.md).</span></span> |
| <span data-ttu-id="9d24a-124">DisableCredentialsDelegation</span><span class="sxs-lookup"><span data-stu-id="9d24a-124">DisableCredentialsDelegation</span></span> | <span data-ttu-id="9d24a-125">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="9d24a-125">**VT\_BOOL**</span></span> | <span data-ttu-id="9d24a-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d24a-126">Read/Write</span></span> | <span data-ttu-id="9d24a-127">No</span><span class="sxs-lookup"><span data-stu-id="9d24a-127">No</span></span> | <span data-ttu-id="9d24a-128">若 **為 True**，則不會將認證傳送至遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="9d24a-128">If **True**, credentials are not sent to the remote server.</span></span> |
| <span data-ttu-id="9d24a-129">EnableFrameBufferRedirection</span><span class="sxs-lookup"><span data-stu-id="9d24a-129">EnableFrameBufferRedirection</span></span> | <span data-ttu-id="9d24a-130">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="9d24a-130">**VT\_BOOL**</span></span> | <span data-ttu-id="9d24a-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d24a-131">Read/Write</span></span> | <span data-ttu-id="9d24a-132">No</span><span class="sxs-lookup"><span data-stu-id="9d24a-132">No</span></span> | <span data-ttu-id="9d24a-133">若 **為 True**，則會嘗試框架緩衝區重新導向。</span><span class="sxs-lookup"><span data-stu-id="9d24a-133">If **True**, frame buffer redirection is attempted.</span></span> <span data-ttu-id="9d24a-134">若是回送連接 (相同電腦同時是用戶端和伺服器) 框架緩衝區重新導向，可讓框架緩衝區的記憶體在會話之間共用。</span><span class="sxs-lookup"><span data-stu-id="9d24a-134">For a loopback connection (the same computer is both client and server) frame buffer redirection allows the memory for the frame buffer to be shared between the sessions.</span></span> |
| <span data-ttu-id="9d24a-135">EnableHardwareMode</span><span class="sxs-lookup"><span data-stu-id="9d24a-135">EnableHardwareMode</span></span> | <span data-ttu-id="9d24a-136">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="9d24a-136">**VT\_BOOL**</span></span>  | <span data-ttu-id="9d24a-137">僅限寫入</span><span class="sxs-lookup"><span data-stu-id="9d24a-137">Write Only</span></span> | <span data-ttu-id="9d24a-138">No</span><span class="sxs-lookup"><span data-stu-id="9d24a-138">No</span></span> | <span data-ttu-id="9d24a-139">若 **為 True**，則會嘗試進行圖形解碼的硬體協助。</span><span class="sxs-lookup"><span data-stu-id="9d24a-139">If **True**, hardware assist with graphics decoding is attempted.</span></span> |
| <span data-ttu-id="9d24a-140">IgnoreCursors</span><span class="sxs-lookup"><span data-stu-id="9d24a-140">IgnoreCursors</span></span> | <span data-ttu-id="9d24a-141">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="9d24a-141">**VT\_BOOL**</span></span> | <span data-ttu-id="9d24a-142">僅限寫入</span><span class="sxs-lookup"><span data-stu-id="9d24a-142">Write Only</span></span> | <span data-ttu-id="9d24a-143">No</span><span class="sxs-lookup"><span data-stu-id="9d24a-143">No</span></span> | <span data-ttu-id="9d24a-144">若 **為 True**，則會忽略遠端伺服器傳送的資料指標。</span><span class="sxs-lookup"><span data-stu-id="9d24a-144">If **True**, cursors sent by the remote server are ignored.</span></span> |
| <span data-ttu-id="9d24a-145">ManualClipboardSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="9d24a-145">ManualClipboardSyncEnabled</span></span> | <span data-ttu-id="9d24a-146">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="9d24a-146">**VT\_BOOL**</span></span> | <span data-ttu-id="9d24a-147">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d24a-147">Read/Write</span></span> | <span data-ttu-id="9d24a-148">Yes</span><span class="sxs-lookup"><span data-stu-id="9d24a-148">Yes</span></span> | <span data-ttu-id="9d24a-149">將此屬性設定為 **True** 表示本機和遠端寫字板將不會自動保持同步。相反地，您必須使用 [**IMsRdpClipboard**](imsrdpclipboard.md) 介面，將剪貼簿格式從本機剪貼簿同步到遠端剪貼簿，並將遠端剪貼簿同步至本機剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="9d24a-149">Setting this property to **True** means that the local and remote clipboards will not be automatically kept in sync. Instead the [**IMsRdpClipboard**](imsrdpclipboard.md) interface must be used to sync clipboard formats from the local clipboard to the remote clipboard and the remote clipboard to the local clipboard.</span></span> |
| <span data-ttu-id="9d24a-150">ZoomLevel</span><span class="sxs-lookup"><span data-stu-id="9d24a-150">ZoomLevel</span></span> | <span data-ttu-id="9d24a-151">\**_VT \_ UI4_*</span><span class="sxs-lookup"><span data-stu-id="9d24a-151">\**_VT\_UI4_*</span></span> | <span data-ttu-id="9d24a-152">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d24a-152">Read/Write</span></span> | <span data-ttu-id="9d24a-153">Yes</span><span class="sxs-lookup"><span data-stu-id="9d24a-153">Yes</span></span> | <span data-ttu-id="9d24a-154">使用 RDP ActiveX 控制項來實行縮放功能。</span><span class="sxs-lookup"><span data-stu-id="9d24a-154">Implements the Zoom feature by using the RDP ActiveX control.</span></span> <span data-ttu-id="9d24a-155">您可以從 RDP 的 **系統** 功能表使用 [縮放] 功能。</span><span class="sxs-lookup"><span data-stu-id="9d24a-155">The Zoom feature is available from the **System** menu of RDP.</span></span> <span data-ttu-id="9d24a-156">**ZoomLevel** 屬性在 RemoteApp 模式和全螢幕模式中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9d24a-156">The **ZoomLevel** property has no effect in RemoteApp mode and full-screen mode.</span></span> <span data-ttu-id="9d24a-157">[**IMsRdpClientAdvancedSettings：： SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) 和 **ZoomLevel** 彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="9d24a-157">[**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) and **ZoomLevel** are mutually exclusive.</span></span> |

## <a name="requirements"></a><span data-ttu-id="9d24a-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d24a-158">Requirements</span></span>



| <span data-ttu-id="9d24a-159">需求</span><span class="sxs-lookup"><span data-stu-id="9d24a-159">Requirement</span></span> | <span data-ttu-id="9d24a-160">值</span><span class="sxs-lookup"><span data-stu-id="9d24a-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d24a-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d24a-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9d24a-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9d24a-162">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d24a-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d24a-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9d24a-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d24a-164">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d24a-165">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9d24a-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d24a-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d24a-166"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="9d24a-167">DLL</span><span class="sxs-lookup"><span data-stu-id="9d24a-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d24a-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d24a-168"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="9d24a-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="9d24a-169">CLSID</span></span><br/>                    | <span data-ttu-id="9d24a-170">CLSID \_ MsRdpClient7NotSafeForScripting 定義為54d38bf7-b1ef-4479-9674-1bd6ea465258</span><span class="sxs-lookup"><span data-stu-id="9d24a-170">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54d38bf7-b1ef-4479-9674-1bd6ea465258</span></span><br/> <span data-ttu-id="9d24a-171">CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="9d24a-171">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="9d24a-172">CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="9d24a-172">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="9d24a-173">IID</span><span class="sxs-lookup"><span data-stu-id="9d24a-173">IID</span></span><br/>                      | <span data-ttu-id="9d24a-174">IID \_ IMsRdpExtendedSettings 定義為302D8188-0052-4807-806A-362B628F9AC5</span><span class="sxs-lookup"><span data-stu-id="9d24a-174">IID\_IMsRdpExtendedSettings is defined as 302D8188-0052-4807-806A-362B628F9AC5</span></span><br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="9d24a-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d24a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d24a-176">**IMsRdpExtendedSettings**</span><span class="sxs-lookup"><span data-stu-id="9d24a-176">**IMsRdpExtendedSettings**</span></span>](imsrdpextendedsettings.md)
</dt> </dl>

 

 





