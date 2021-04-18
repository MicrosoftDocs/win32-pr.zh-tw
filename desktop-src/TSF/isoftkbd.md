---
title: 'ISoftKbd 介面 (Softkbdc .h) '
description: 應用程式和文字服務會使用 ISoftKbd 介面來執行軟鍵盤。
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- ISoftKbd 介面文字服務架構
- ISoftKbd 介面文字服務架構，說明
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965690"
---
# <a name="isoftkbd-interface"></a><span data-ttu-id="1bba4-105">ISoftKbd 介面</span><span class="sxs-lookup"><span data-stu-id="1bba4-105">ISoftKbd interface</span></span>

<span data-ttu-id="1bba4-106">應用程式和文字服務會使用 **ISoftKbd** 介面來執行軟鍵盤。</span><span class="sxs-lookup"><span data-stu-id="1bba4-106">The **ISoftKbd** interface is used by applications and text services to implement a soft keyboard.</span></span>

## <a name="members"></a><span data-ttu-id="1bba4-107">成員</span><span class="sxs-lookup"><span data-stu-id="1bba4-107">Members</span></span>

<span data-ttu-id="1bba4-108">**ISoftKbd** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1bba4-108">The **ISoftKbd** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1bba4-109">**ISoftKbd** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1bba4-109">**ISoftKbd** also has these types of members:</span></span>

-   [<span data-ttu-id="1bba4-110">方法</span><span class="sxs-lookup"><span data-stu-id="1bba4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1bba4-111">方法</span><span class="sxs-lookup"><span data-stu-id="1bba4-111">Methods</span></span>

<span data-ttu-id="1bba4-112">**ISoftKbd** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1bba4-112">The **ISoftKbd** interface has these methods.</span></span>



| <span data-ttu-id="1bba4-113">方法</span><span class="sxs-lookup"><span data-stu-id="1bba4-113">Method</span></span>                                                                                        | <span data-ttu-id="1bba4-114">描述</span><span class="sxs-lookup"><span data-stu-id="1bba4-114">Description</span></span>                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bba4-115">**AdviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="1bba4-115">**AdviseSoftKeyboardEventSink**</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)                   | <span data-ttu-id="1bba4-116">安裝軟鍵盤事件接收器，以從螢幕小鍵盤處理 OnKeySelection 通知。</span><span class="sxs-lookup"><span data-stu-id="1bba4-116">Installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span><br/> |
| [<span data-ttu-id="1bba4-117">**CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="1bba4-117">**CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md) | <span data-ttu-id="1bba4-118">從指定的資源建立軟鍵盤版面配置。</span><span class="sxs-lookup"><span data-stu-id="1bba4-118">Creates a soft keyboard layout from the specified resource.</span></span><br/>                                        |
| [<span data-ttu-id="1bba4-119">**CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="1bba4-119">**CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | <span data-ttu-id="1bba4-120">從指定的 XML 檔案建立軟鍵盤版面配置。</span><span class="sxs-lookup"><span data-stu-id="1bba4-120">Creates a soft keyboard layout from the specified XML file.</span></span><br/>                                        |
| [<span data-ttu-id="1bba4-121">**CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="1bba4-121">**CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)                         | <span data-ttu-id="1bba4-122">建立軟鍵盤視窗。</span><span class="sxs-lookup"><span data-stu-id="1bba4-122">Creates a soft keyboard window.</span></span><br/>                                                                    |
| [<span data-ttu-id="1bba4-123">**DestroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="1bba4-123">**DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)                       | <span data-ttu-id="1bba4-124">終結軟鍵盤視窗。</span><span class="sxs-lookup"><span data-stu-id="1bba4-124">Destroys a soft keyboard window.</span></span><br/>                                                                   |
| [<span data-ttu-id="1bba4-125">**EnumSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="1bba4-125">**EnumSoftKeyboard**</span></span>](isoftkbd-enumsoftkeyboard.md)                                         | <span data-ttu-id="1bba4-126">列舉支援指定語言的可能軟鍵盤。</span><span class="sxs-lookup"><span data-stu-id="1bba4-126">Enumerates the possible soft keyboards that support the specified language.</span></span><br/>                        |
| [<span data-ttu-id="1bba4-127">**GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="1bba4-127">**GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)                               | <span data-ttu-id="1bba4-128">抓取與所提供色彩類型對應的軟鍵盤色彩。</span><span class="sxs-lookup"><span data-stu-id="1bba4-128">Retrieves the soft keyboard color corresponding to the supplied color type.</span></span><br/>                        |
| [<span data-ttu-id="1bba4-129">**GetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="1bba4-129">**GetSoftKeyboardPosSize**</span></span>](isoftkbd-getsoftkeyboardpossize.md)                             | <span data-ttu-id="1bba4-130">抓取軟鍵盤的開始位置和大小。</span><span class="sxs-lookup"><span data-stu-id="1bba4-130">Retrieves the starting position and size of a soft keyboard.</span></span><br/>                                       |
| [<span data-ttu-id="1bba4-131">**GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="1bba4-131">**GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)                           | <span data-ttu-id="1bba4-132">抓取軟鍵盤所使用的文字字型。</span><span class="sxs-lookup"><span data-stu-id="1bba4-132">Retrieves the text font used by a soft keyboard.</span></span><br/>                                                   |
| [<span data-ttu-id="1bba4-133">**GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="1bba4-133">**GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)                           | <span data-ttu-id="1bba4-134">抓取軟鍵盤的類型模式。</span><span class="sxs-lookup"><span data-stu-id="1bba4-134">Retrieves the type mode for a soft keyboard.</span></span><br/>                                                       |
| [<span data-ttu-id="1bba4-135">**初始化**</span><span class="sxs-lookup"><span data-stu-id="1bba4-135">**Initialize**</span></span>](isoftkbd-initialize.md)                                                     | <span data-ttu-id="1bba4-136">初始化軟鍵盤的所有必要欄位，並產生標準的軟鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="1bba4-136">Initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span><br/> |
| [<span data-ttu-id="1bba4-137">**SelectSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="1bba4-137">**SelectSoftKeyboard**</span></span>](isoftkbd-selectsoftkeyboard.md)                                     | <span data-ttu-id="1bba4-138">選取指定的軟鍵盤。</span><span class="sxs-lookup"><span data-stu-id="1bba4-138">Selects the specified soft keyboard.</span></span><br/>                                                               |
| [<span data-ttu-id="1bba4-139">**SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="1bba4-139">**SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)                                 | <span data-ttu-id="1bba4-140">從軟鍵盤的版面配置設定標籤文字。</span><span class="sxs-lookup"><span data-stu-id="1bba4-140">Sets the label text from the layout for a soft keyboard.</span></span><br/>                                           |
| [<span data-ttu-id="1bba4-141">**SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="1bba4-141">**SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)           | <span data-ttu-id="1bba4-142">設定用來描述軟鍵盤的標籤和文字的組合。</span><span class="sxs-lookup"><span data-stu-id="1bba4-142">Sets a combination of label and text used to describe a soft keyboard.</span></span><br/>                             |
| [<span data-ttu-id="1bba4-143">**SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="1bba4-143">**SetSoftKeyboardColors**</span></span>](isoftkbd-setsoftkeyboardcolors.md)                               | <span data-ttu-id="1bba4-144">設定對應于所提供色彩類型的軟鍵盤色彩。</span><span class="sxs-lookup"><span data-stu-id="1bba4-144">Sets the soft keyboard color corresponding to the supplied color type.</span></span><br/>                             |
| [<span data-ttu-id="1bba4-145">**SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="1bba4-145">**SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)                             | <span data-ttu-id="1bba4-146">設定軟鍵盤的開始位置和大小。</span><span class="sxs-lookup"><span data-stu-id="1bba4-146">Sets the starting position and size of a soft keyboard.</span></span><br/>                                            |
| [<span data-ttu-id="1bba4-147">**SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="1bba4-147">**SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)                           | <span data-ttu-id="1bba4-148">設定軟鍵盤所使用的文字字型。</span><span class="sxs-lookup"><span data-stu-id="1bba4-148">Sets the text font used by a soft keyboard.</span></span><br/>                                                        |
| [<span data-ttu-id="1bba4-149">**SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="1bba4-149">**SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)                           | <span data-ttu-id="1bba4-150">設定軟鍵盤的類型模式。</span><span class="sxs-lookup"><span data-stu-id="1bba4-150">Sets the type mode for a soft keyboard.</span></span><br/>                                                            |
| [<span data-ttu-id="1bba4-151">**ShowKeysForKeyScanMode**</span><span class="sxs-lookup"><span data-stu-id="1bba4-151">**ShowKeysForKeyScanMode**</span></span>](isoftkbd-showkeysforkeyscanmode.md)                             | <span data-ttu-id="1bba4-152">顯示軟鍵盤的金鑰掃描模式所使用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1bba4-152">Displays the keys used for the key scan mode for a soft keyboard.</span></span><br/>                                  |
| [<span data-ttu-id="1bba4-153">**ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="1bba4-153">**ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)                                         | <span data-ttu-id="1bba4-154">顯示軟鍵盤。</span><span class="sxs-lookup"><span data-stu-id="1bba4-154">Displays a soft keyboard.</span></span><br/>                                                                          |
| [<span data-ttu-id="1bba4-155">**UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="1bba4-155">**UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)               | <span data-ttu-id="1bba4-156">移除軟鍵盤事件接收器。</span><span class="sxs-lookup"><span data-stu-id="1bba4-156">Removes a soft keyboard event sink.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="1bba4-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bba4-157">Requirements</span></span>



| <span data-ttu-id="1bba4-158">需求</span><span class="sxs-lookup"><span data-stu-id="1bba4-158">Requirement</span></span> | <span data-ttu-id="1bba4-159">值</span><span class="sxs-lookup"><span data-stu-id="1bba4-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bba4-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bba4-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1bba4-161">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bba4-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1bba4-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bba4-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1bba4-163">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bba4-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1bba4-164">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1bba4-164">Redistributable</span></span><br/>          | <span data-ttu-id="1bba4-165">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="1bba4-165">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1bba4-166">標頭</span><span class="sxs-lookup"><span data-stu-id="1bba4-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bba4-167"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bba4-167"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1bba4-168">Idl</span><span class="sxs-lookup"><span data-stu-id="1bba4-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1bba4-169"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1bba4-169"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="1bba4-170">DLL</span><span class="sxs-lookup"><span data-stu-id="1bba4-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bba4-171"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bba4-171"><dt>Softkbd.dll</dt></span></span> </dl> |



 

