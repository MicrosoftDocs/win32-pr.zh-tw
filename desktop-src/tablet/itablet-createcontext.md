---
description: 建立描述指定之平板電腦裝置的內容物件。
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: ITablet：： CreateCoNtext 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852168"
---
# <a name="itabletcreatecontext-method"></a><span data-ttu-id="4008e-103">ITablet：： CreateCoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="4008e-103">ITablet::CreateContext method</span></span>

<span data-ttu-id="4008e-104">建立描述指定之平板電腦裝置的內容物件。</span><span class="sxs-lookup"><span data-stu-id="4008e-104">Creates a context object that describes the specified tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4008e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4008e-105">Syntax</span></span>


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="4008e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4008e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4008e-107">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4008e-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-108">Tablet 內容將附加的視窗。</span><span class="sxs-lookup"><span data-stu-id="4008e-108">The window to which the tablet context will be attached.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-109">*prcInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4008e-109">*prcInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-110">\[在中，唯一\]</span><span class="sxs-lookup"><span data-stu-id="4008e-110">\[in, unique\]</span></span>

<span data-ttu-id="4008e-111">筆墨輸入矩形。</span><span class="sxs-lookup"><span data-stu-id="4008e-111">The ink input rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-112">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4008e-112">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-113">設定 tablet coNtext 選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="4008e-113">Flags that set tablet context options.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-114">*pTCS* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4008e-114">*pTCS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-115">\[在中，唯一\]</span><span class="sxs-lookup"><span data-stu-id="4008e-115">\[in, unique\]</span></span>

<span data-ttu-id="4008e-116">要建立之平板電腦內容的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4008e-116">Detailed information about the tablet context to create.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-117">*cet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4008e-117">*cet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-118">值，這個值會啟用或停用傳送至視窗的內容訊息。</span><span class="sxs-lookup"><span data-stu-id="4008e-118">Value that enables or disables context messages being sent to the window.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-119">*ppCtx* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4008e-119">*ppCtx* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-120">新建立的平板電腦內容指標。</span><span class="sxs-lookup"><span data-stu-id="4008e-120">A pointer to the newly create tablet context.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-121">*pTcid* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4008e-121">*pTcid* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-122">可唯一識別平板電腦的值。</span><span class="sxs-lookup"><span data-stu-id="4008e-122">Value that uniquely identifies the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-123">*ppPD* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4008e-123">*ppPD* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-124">每個封包中包含哪些資料的相關資訊指標。</span><span class="sxs-lookup"><span data-stu-id="4008e-124">Pointer to information about what data is contained in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="4008e-125">*pSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4008e-125">*pSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4008e-126">將傳送通知訊息的 [**ITabletEventSink**](itableteventsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4008e-126">The [**ITabletEventSink**](itableteventsink.md) object where notification messages will be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4008e-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="4008e-127">Return value</span></span>

<span data-ttu-id="4008e-128">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4008e-128">This method can return one of these values.</span></span>



| <span data-ttu-id="4008e-129">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4008e-129">Return code</span></span>                                                                            | <span data-ttu-id="4008e-130">Description</span><span class="sxs-lookup"><span data-stu-id="4008e-130">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4008e-131"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4008e-131"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4008e-132">成功。</span><span class="sxs-lookup"><span data-stu-id="4008e-132">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="4008e-133"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="4008e-133"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4008e-134">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4008e-134">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4008e-135">備註</span><span class="sxs-lookup"><span data-stu-id="4008e-135">Remarks</span></span>

<span data-ttu-id="4008e-136">一般而言，應用程式會從 [**ITablet：： GetDefaultCoNtextSettings 方法**](itablet-getdefaultcontextsettings.md)取得預設值、修改值以符合其需求，然後將修改過的設定結構傳遞至 **ITablet：： CreateCoNtext 方法**。</span><span class="sxs-lookup"><span data-stu-id="4008e-136">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the **ITablet::CreateContext Method**.</span></span>

> [!Note]  
> <span data-ttu-id="4008e-137">呼叫 **ITablet：： CreateCoNtext 方法** 時，您必須執行 [**ITabletEventSink 介面**](itableteventsink.md)。</span><span class="sxs-lookup"><span data-stu-id="4008e-137">You must implement the [**ITabletEventSink Interface**](itableteventsink.md) when calling the **ITablet::CreateContext Method**.</span></span>

 

<span data-ttu-id="4008e-138">*>dwoptions* 參數是一組用來描述內容選項的位旗標。</span><span class="sxs-lookup"><span data-stu-id="4008e-138">The *dwOptions* parameter is a set of bit flags that describe context options.</span></span> <span data-ttu-id="4008e-139">下表描述這些旗標。</span><span class="sxs-lookup"><span data-stu-id="4008e-139">The following table describes these flags.</span></span>



| <span data-ttu-id="4008e-140">旗標名稱</span><span class="sxs-lookup"><span data-stu-id="4008e-140">Flag Name</span></span>                                | <span data-ttu-id="4008e-141">值</span><span class="sxs-lookup"><span data-stu-id="4008e-141">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="4008e-142">描述</span><span class="sxs-lookup"><span data-stu-id="4008e-142">Description</span></span>                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4008e-143">TCXO \_ 邊界</span><span class="sxs-lookup"><span data-stu-id="4008e-143">TCXO\_MARGIN</span></span><br/>                  | <span data-ttu-id="4008e-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4008e-144">0x00000001</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-145">指定平板電腦上的輸入內容將會有邊界。</span><span class="sxs-lookup"><span data-stu-id="4008e-145">Specifies that the input context on the tablet will have a margin.</span></span> <span data-ttu-id="4008e-146">邊界是指定之輸入區域以外的區域，其中的事件將會對應至輸入區域的邊緣。</span><span class="sxs-lookup"><span data-stu-id="4008e-146">The margin is an area outside the specified input area where events will be mapped to the edge of the input area.</span></span> <span data-ttu-id="4008e-147">這項功能可讓您更輕鬆地在內容邊緣輸入點。</span><span class="sxs-lookup"><span data-stu-id="4008e-147">This feature makes it easier to input points at the edge of the context.</span></span><br/> |
| <span data-ttu-id="4008e-148">TCXO \_ PREHOOK</span><span class="sxs-lookup"><span data-stu-id="4008e-148">TCXO\_PREHOOK</span></span><br/>                 | <span data-ttu-id="4008e-149">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4008e-149">0x00000002</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-150">Prehook 會在一般內容和 posthooks 之前取得封包。</span><span class="sxs-lookup"><span data-stu-id="4008e-150">Prehook gets packets before regular contexts and posthooks.</span></span> <span data-ttu-id="4008e-151">他們會依照建立的順序取得封包。</span><span class="sxs-lookup"><span data-stu-id="4008e-151">They get packets in the order of their creation.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="4008e-152">TCXO 資料 \_ 指標 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="4008e-152">TCXO\_CURSOR\_STATE</span></span><br/>           | <span data-ttu-id="4008e-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4008e-153">0x00000004</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-154">即使資料指標已啟動，TC 也會傳回封包。</span><span class="sxs-lookup"><span data-stu-id="4008e-154">The TC will return packets even if the cursor is up.</span></span> <span data-ttu-id="4008e-155">根據預設，在游標關閉時，TC 只會傳回封包。</span><span class="sxs-lookup"><span data-stu-id="4008e-155">By default, a TC will only return packets when the cursor is down.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="4008e-156">TCXO \_ 無 \_ 游標 \_ 向下鍵</span><span class="sxs-lookup"><span data-stu-id="4008e-156">TCXO\_NO\_CURSOR\_DOWN</span></span><br/>        | <span data-ttu-id="4008e-157">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4008e-157">0x00000008</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-158">當資料指標關閉時，TC 不會傳回封包。</span><span class="sxs-lookup"><span data-stu-id="4008e-158">The TC will not return packets when the cursor is down.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="4008e-159">TCXO \_ 非 \_ 整合式</span><span class="sxs-lookup"><span data-stu-id="4008e-159">TCXO\_NON\_INTEGRATED</span></span><br/>         | <span data-ttu-id="4008e-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4008e-160">0x00000010</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-161">內容將不會整合。</span><span class="sxs-lookup"><span data-stu-id="4008e-161">The context will be non-integrated.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="4008e-162">TCXO \_ POSTHOOK</span><span class="sxs-lookup"><span data-stu-id="4008e-162">TCXO\_POSTHOOK</span></span><br/>                | <span data-ttu-id="4008e-163">0x00000020</span><span class="sxs-lookup"><span data-stu-id="4008e-163">0x00000020</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-164">Posthooks 會在一般的 tablet 內容之後，但在系統內容之前取得封包。</span><span class="sxs-lookup"><span data-stu-id="4008e-164">Posthooks get packets after regular tablet contexts but before the system context.</span></span> <span data-ttu-id="4008e-165">它們會以建立的相反順序取得封包。</span><span class="sxs-lookup"><span data-stu-id="4008e-165">They get packets in the reverse order of their creation.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="4008e-166">TCXO \_ 不要 \_ 顯示資料 \_ 指標</span><span class="sxs-lookup"><span data-stu-id="4008e-166">TCXO\_DONT\_SHOW\_CURSOR</span></span><br/>      | <span data-ttu-id="4008e-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="4008e-167">0x00000080</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-168">TC 不會設定資料指標的位置。</span><span class="sxs-lookup"><span data-stu-id="4008e-168">The TC will not set the cursor position.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="4008e-169">TCXO 不會 \_ \_ 驗證 \_ TCS</span><span class="sxs-lookup"><span data-stu-id="4008e-169">TCXO\_DONT\_VALIDATE\_TCS</span></span><br/>     | <span data-ttu-id="4008e-170">0x00000100</span><span class="sxs-lookup"><span data-stu-id="4008e-170">0x00000100</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-171">TC 不會針對裝置支援的屬性驗證 tablet 內容設定中傳遞的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4008e-171">The TC will not validate the GUIDS passed in the tablet context settings against the supported properties of the device.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4008e-172">TCXO \_ 允許 \_ 筆觸</span><span class="sxs-lookup"><span data-stu-id="4008e-172">TCXO\_ALLOW\_FLICKS</span></span><br/>           | <span data-ttu-id="4008e-173">0x00000400</span><span class="sxs-lookup"><span data-stu-id="4008e-173">0x00000400</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-174">TC 將允許執行筆觸偵測 (預設只允許在系統內容) ，而且用戶端會取得 SE 筆觸 \_ 事件。</span><span class="sxs-lookup"><span data-stu-id="4008e-174">The TC will allow flick detection to take place (by default this is only allowed on system contexts), and the client will get SE\_FLICK events.</span></span><br/>                                                                                                               |
| <span data-ttu-id="4008e-175">TCXO \_ 允許 \_ 意見反應 \_ 點擊</span><span class="sxs-lookup"><span data-stu-id="4008e-175">TCXO\_ALLOW\_FEEDBACK\_TAPS</span></span><br/>   | <span data-ttu-id="4008e-176">0x00000800</span><span class="sxs-lookup"><span data-stu-id="4008e-176">0x00000800</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-177">TC 將允許顯示畫筆意見反應。</span><span class="sxs-lookup"><span data-stu-id="4008e-177">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="4008e-178">根據預設，這只允許在系統內容上使用。</span><span class="sxs-lookup"><span data-stu-id="4008e-178">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="4008e-179">TCXO \_ 允許 \_ 意見反應 \_ 桶</span><span class="sxs-lookup"><span data-stu-id="4008e-179">TCXO\_ALLOW\_FEEDBACK\_BARREL</span></span><br/> | <span data-ttu-id="4008e-180">0x00001000</span><span class="sxs-lookup"><span data-stu-id="4008e-180">0x00001000</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="4008e-181">TC 將允許顯示畫筆意見反應。</span><span class="sxs-lookup"><span data-stu-id="4008e-181">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="4008e-182">根據預設，這只允許在系統內容上使用。</span><span class="sxs-lookup"><span data-stu-id="4008e-182">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="4008e-183">TCXO \_ 全部</span><span class="sxs-lookup"><span data-stu-id="4008e-183">TCXO\_ALL</span></span><br/>                     | <span data-ttu-id="4008e-184">TCXO \_ MARGIN \| TCXO \_ PREHOOK \| TCXO 資料 \_ 指標 \_ 狀態 \| TCXO \_ 沒有 \_ 游標 \_ 向下 \| TCXO \_ 非整合式 \_ \| TCXO \_ POSTHOOK TCXO 不顯示資料 \| \_ \_ \_ 指標 TCXO 不 \| \_ \_ 驗證 \_ TCS</span><span class="sxs-lookup"><span data-stu-id="4008e-184">TCXO\_MARGIN \| TCXO\_PREHOOK \| TCXO\_CURSOR\_STATE \| TCXO\_NO\_CURSOR\_DOWN \| TCXO\_NON\_INTEGRATED \| TCXO\_POSTHOOK \| TCXO\_DONT\_SHOW\_CURSOR \| TCXO\_DONT\_VALIDATE\_TCS</span></span><br/> | <span data-ttu-id="4008e-185">所有已定義的 tablet coNtext 選項。</span><span class="sxs-lookup"><span data-stu-id="4008e-185">All defined tablet context options.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="4008e-186">TCXO \_ 掛勾</span><span class="sxs-lookup"><span data-stu-id="4008e-186">TCXO\_HOOK</span></span><br/>                    | <span data-ttu-id="4008e-187">TCXO \_ PREHOOK \| TCXO \_ POSTHOOK</span><span class="sxs-lookup"><span data-stu-id="4008e-187">TCXO\_PREHOOK \| TCXO\_POSTHOOK</span></span><br/>                                                                                                                                                    | <span data-ttu-id="4008e-188">結合了預先攔截和後置攔截功能。</span><span class="sxs-lookup"><span data-stu-id="4008e-188">Combines pre-hook and post-hook functionality.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="4008e-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="4008e-189">Requirements</span></span>



| <span data-ttu-id="4008e-190">需求</span><span class="sxs-lookup"><span data-stu-id="4008e-190">Requirement</span></span> | <span data-ttu-id="4008e-191">值</span><span class="sxs-lookup"><span data-stu-id="4008e-191">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4008e-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4008e-192">Minimum supported client</span></span><br/> | <span data-ttu-id="4008e-193">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4008e-193">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4008e-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4008e-194">Minimum supported server</span></span><br/> | <span data-ttu-id="4008e-195">都不支援</span><span class="sxs-lookup"><span data-stu-id="4008e-195">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4008e-196">程式庫</span><span class="sxs-lookup"><span data-stu-id="4008e-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="4008e-197"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4008e-197"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4008e-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4008e-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4008e-199">**ITablet 介面**</span><span class="sxs-lookup"><span data-stu-id="4008e-199">**ITablet Interface**</span></span>](itablet.md)
</dt> <dt>

[<span data-ttu-id="4008e-200">**內容 \_ 啟用 \_ 類型列舉**</span><span class="sxs-lookup"><span data-stu-id="4008e-200">**CONTEXT\_ENABLE\_TYPE Enumeration**</span></span>](context-enable-type.md)
</dt> <dt>

[<span data-ttu-id="4008e-201">**TABLET \_ 內容 \_ 設定結構**</span><span class="sxs-lookup"><span data-stu-id="4008e-201">**TABLET\_CONTEXT\_SETTINGS Structure**</span></span>](tablet-context-settings.md)
</dt> <dt>

[<span data-ttu-id="4008e-202">**封包 \_ 描述結構**</span><span class="sxs-lookup"><span data-stu-id="4008e-202">**PACKET\_DESCRIPTION Structure**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[<span data-ttu-id="4008e-203">**ITabletCoNtextP 介面**</span><span class="sxs-lookup"><span data-stu-id="4008e-203">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="4008e-204">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="4008e-204">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




