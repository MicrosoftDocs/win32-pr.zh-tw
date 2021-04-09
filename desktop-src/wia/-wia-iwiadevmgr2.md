---
description: IWiaDevMgr2 介面是用來建立及管理影像取得裝置，並註冊以接收裝置事件。
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: 'IWiaDevMgr2 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849355"
---
# <a name="iwiadevmgr2-interface"></a><span data-ttu-id="3e93c-103">IWiaDevMgr2 介面</span><span class="sxs-lookup"><span data-stu-id="3e93c-103">IWiaDevMgr2 interface</span></span>

<span data-ttu-id="3e93c-104">**IWiaDevMgr2** 介面是用來建立及管理影像取得裝置，並註冊以接收裝置事件。</span><span class="sxs-lookup"><span data-stu-id="3e93c-104">The **IWiaDevMgr2** interface is used to create and manage image acquisition devices and to register to receive device events.</span></span>

## <a name="members"></a><span data-ttu-id="3e93c-105">成員</span><span class="sxs-lookup"><span data-stu-id="3e93c-105">Members</span></span>

<span data-ttu-id="3e93c-106">**IWiaDevMgr2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3e93c-106">The **IWiaDevMgr2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3e93c-107">**IWiaDevMgr2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e93c-107">**IWiaDevMgr2** also has these types of members:</span></span>

-   [<span data-ttu-id="3e93c-108">方法</span><span class="sxs-lookup"><span data-stu-id="3e93c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e93c-109">方法</span><span class="sxs-lookup"><span data-stu-id="3e93c-109">Methods</span></span>

<span data-ttu-id="3e93c-110">**IWiaDevMgr2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3e93c-110">The **IWiaDevMgr2** interface has these methods.</span></span>



| <span data-ttu-id="3e93c-111">方法</span><span class="sxs-lookup"><span data-stu-id="3e93c-111">Method</span></span>                                                                                    | <span data-ttu-id="3e93c-112">描述</span><span class="sxs-lookup"><span data-stu-id="3e93c-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e93c-113">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="3e93c-113">**CreateDevice**</span></span>](-wia-iwiadevmgr2-createdevice.md)                                     | <span data-ttu-id="3e93c-114">針對 WIA 2.0 裝置建立 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="3e93c-114">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="3e93c-115">**EnumDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="3e93c-115">**EnumDeviceInfo**</span></span>](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | <span data-ttu-id="3e93c-116">針對每個可用的 WIA 2.0 裝置建立屬性資訊的列舉值。</span><span class="sxs-lookup"><span data-stu-id="3e93c-116">Creates an enumerator of property information for each available WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="3e93c-117">**GetImageDlg**</span><span class="sxs-lookup"><span data-stu-id="3e93c-117">**GetImageDlg**</span></span>](-wia-iwiadevmgr2-getimagedlg.md)                                       | <span data-ttu-id="3e93c-118">[**IWiaDevMgr2：： GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)方法會顯示一或多個對話方塊，讓使用者從 WIA 2.0 裝置取得影像，並將影像寫入指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="3e93c-118">The [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method displays one or more dialog boxes that enable a user to acquire an image from a WIA 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="3e93c-119">這個方法會擴充 [**IWiaDevMgr2：： SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) 的功能，以在單一 API 呼叫中封裝取得影像。</span><span class="sxs-lookup"><span data-stu-id="3e93c-119">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span> <br/> |
| [<span data-ttu-id="3e93c-120">**RegisterEventCallbackCLSID**</span><span class="sxs-lookup"><span data-stu-id="3e93c-120">**RegisterEventCallbackCLSID**</span></span>](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | <span data-ttu-id="3e93c-121">[**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)方法會註冊應用程式以接收事件，即使應用程式並未執行也一樣。</span><span class="sxs-lookup"><span data-stu-id="3e93c-121">The [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) method registers an application to receive events even if the application is not running.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="3e93c-122">**RegisterEventCallbackInterface**</span><span class="sxs-lookup"><span data-stu-id="3e93c-122">**RegisterEventCallbackInterface**</span></span>](-wia-iwiadevmgr2-registereventcallbackinterface.md) | <span data-ttu-id="3e93c-123">註冊 WIA 2.0 事件通知的執行中應用程式。</span><span class="sxs-lookup"><span data-stu-id="3e93c-123">Registers a running application for WIA 2.0 event notification.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="3e93c-124">**RegisterEventCallbackProgram**</span><span class="sxs-lookup"><span data-stu-id="3e93c-124">**RegisterEventCallbackProgram**</span></span>](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | <span data-ttu-id="3e93c-125">[**IWiaDevMgr2：： RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)方法會註冊應用程式以接收裝置事件。</span><span class="sxs-lookup"><span data-stu-id="3e93c-125">The [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method registers an application to receive device events.</span></span> <span data-ttu-id="3e93c-126">它主要是為了提供與未針對 WIA 2.0 撰寫之應用程式的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="3e93c-126">It is primarily provided for backward compatibility with applications that were not written for WIA 2.0.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="3e93c-127">**SelectDeviceDlg**</span><span class="sxs-lookup"><span data-stu-id="3e93c-127">**SelectDeviceDlg**</span></span>](-wia-iwiadevmgr2-selectdevicedlg.md)                               | <span data-ttu-id="3e93c-128">顯示對話方塊，讓使用者選取硬體裝置以取得影像。</span><span class="sxs-lookup"><span data-stu-id="3e93c-128">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="3e93c-129">**SelectDeviceDlgID**</span><span class="sxs-lookup"><span data-stu-id="3e93c-129">**SelectDeviceDlgID**</span></span>](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | <span data-ttu-id="3e93c-130">顯示對話方塊，讓使用者選取硬體裝置以取得影像。</span><span class="sxs-lookup"><span data-stu-id="3e93c-130">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="3e93c-131">備註</span><span class="sxs-lookup"><span data-stu-id="3e93c-131">Remarks</span></span>

<span data-ttu-id="3e93c-132">**IWiaDevMgr2** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。</span><span class="sxs-lookup"><span data-stu-id="3e93c-132">The **IWiaDevMgr2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="3e93c-133">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="3e93c-133">IUnknown Methods</span></span>                                        | <span data-ttu-id="3e93c-134">Description</span><span class="sxs-lookup"><span data-stu-id="3e93c-134">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3e93c-135">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="3e93c-135">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="3e93c-136">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3e93c-136">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="3e93c-137">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="3e93c-137">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="3e93c-138">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="3e93c-138">Increments reference count.</span></span>               |
| [<span data-ttu-id="3e93c-139">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="3e93c-139">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="3e93c-140">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="3e93c-140">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="3e93c-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e93c-141">Requirements</span></span>



| <span data-ttu-id="3e93c-142">需求</span><span class="sxs-lookup"><span data-stu-id="3e93c-142">Requirement</span></span> | <span data-ttu-id="3e93c-143">值</span><span class="sxs-lookup"><span data-stu-id="3e93c-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e93c-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e93c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3e93c-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e93c-145">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e93c-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e93c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3e93c-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e93c-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3e93c-148">標頭</span><span class="sxs-lookup"><span data-stu-id="3e93c-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e93c-149"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="3e93c-149"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e93c-150">Idl</span><span class="sxs-lookup"><span data-stu-id="3e93c-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e93c-151"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e93c-151"><dt>Wia.idl</dt></span></span> </dl> |



 

 
