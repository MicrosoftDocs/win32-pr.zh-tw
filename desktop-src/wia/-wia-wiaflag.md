---
description: IWiaDevMgr：： GetImageDlg、IWiaDevMgr2：： GetImageDlg、IWiaItem：:D eviceDlg 和 IWiaItem2：:D eviceDlg 方法用來控制對話方塊作業的旗標。
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: 'WiaFlag (Wiadef) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986354"
---
# <a name="wiaflag"></a><span data-ttu-id="53267-103">WiaFlag</span><span class="sxs-lookup"><span data-stu-id="53267-103">WiaFlag</span></span>

<span data-ttu-id="53267-104">[**IWiaDevMgr：： GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg)、 [**IWiaDevMgr2：： GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)、 [**IWiaItem：:D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)和 [**IWiaItem2：:D evicedlg**](-wia-iwiaitem2-devicedlg.md)方法用來控制對話方塊作業的旗標。</span><span class="sxs-lookup"><span data-stu-id="53267-104">Flags used by the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg), and [**IWiaItem2::DeviceDlg**](-wia-iwiaitem2-devicedlg.md) methods to control the dialog box operation.</span></span>



| <span data-ttu-id="53267-105">常數</span><span class="sxs-lookup"><span data-stu-id="53267-105">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="53267-106">描述</span><span class="sxs-lookup"><span data-stu-id="53267-106">Description</span></span>                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <span data-ttu-id="53267-107"><dt>**WIA \_ 裝置 \_ 對話方塊 \_ 單一 \_ 影像**</dt></span><span class="sxs-lookup"><span data-stu-id="53267-107"><dt>**WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE**</dt></span></span> </dl>     | <span data-ttu-id="53267-108">在 [裝置映射取得] 對話方塊中，將影像選取範圍限制為單一影像。</span><span class="sxs-lookup"><span data-stu-id="53267-108">Restrict image selection to a single image in the device image acquisition dialog box.</span></span><br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <span data-ttu-id="53267-109"><dt>**WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="53267-109"><dt>**WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI**</dt></span></span> </dl> | <span data-ttu-id="53267-110">使用系統 UI （如果有的話），而不是廠商提供的 UI。</span><span class="sxs-lookup"><span data-stu-id="53267-110">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="53267-111">如果系統 UI 無法使用，則會使用廠商 UI。</span><span class="sxs-lookup"><span data-stu-id="53267-111">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="53267-112">如果沒有可用的 UI，函數會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="53267-112">If neither UI is available, the function returns E\_NOTIMPL.</span></span><br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <span data-ttu-id="53267-113"><dt>**WIA \_ 選取 \_ 裝置 \_ NODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="53267-113"><dt>**WIA\_SELECT\_DEVICE\_NODEFAULT**</dt></span></span> </dl>               | <span data-ttu-id="53267-114">強制 [**IWiaDevMgr：： GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) 或 [**IWiaDevMgr2：： GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) 方法顯示 [ **選取裝置** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="53267-114">Force the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) or [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method to display the **Select Device** dialog box.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="53267-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="53267-115">Requirements</span></span>



| <span data-ttu-id="53267-116">需求</span><span class="sxs-lookup"><span data-stu-id="53267-116">Requirement</span></span> | <span data-ttu-id="53267-117">值</span><span class="sxs-lookup"><span data-stu-id="53267-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53267-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53267-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53267-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53267-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="53267-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53267-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53267-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53267-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="53267-122">標頭</span><span class="sxs-lookup"><span data-stu-id="53267-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53267-123"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="53267-123"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




