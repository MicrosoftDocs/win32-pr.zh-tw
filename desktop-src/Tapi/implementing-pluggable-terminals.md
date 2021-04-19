---
description: 插入式終端機實施的一般需求如下所示。
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: 執行可插入的終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 494b2f6bc5ccb214bc7101f570a4db3037fd8cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993185"
---
# <a name="implementing-pluggable-terminals"></a><span data-ttu-id="0faf2-103">執行可插入的終端機</span><span class="sxs-lookup"><span data-stu-id="0faf2-103">Implementing Pluggable Terminals</span></span>

<span data-ttu-id="0faf2-104">插入式終端機實施的一般需求為：</span><span class="sxs-lookup"><span data-stu-id="0faf2-104">The general requirements for pluggable terminal implementation are:</span></span>

-   <span data-ttu-id="0faf2-105">可插入的終端機基礎串流程式碼應符合所需 Msp 的功能。</span><span class="sxs-lookup"><span data-stu-id="0faf2-105">A pluggable terminal's underlying streaming code should match the capabilities of the desired MSPs.</span></span>
-   <span data-ttu-id="0faf2-106">終端機必須使用 DirectShow 篩選器來處理大部分的 Msp (這是在) 上假設。</span><span class="sxs-lookup"><span data-stu-id="0faf2-106">The terminal must use DirectShow filters to work with most MSPs (this is assumed from here on).</span></span>
-   <span data-ttu-id="0faf2-107">音訊終端機必須支援 8 kHz 16 位 mono 線性 PCM，才能進行大部分的 Msp。</span><span class="sxs-lookup"><span data-stu-id="0faf2-107">Audio terminals must support 8 kHz 16-bit mono linear PCM for most MSPs.</span></span>
-   <span data-ttu-id="0faf2-108">終端機應該藉由執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)來啟用自由執行緒封送處理。</span><span class="sxs-lookup"><span data-stu-id="0faf2-108">The terminal should enable free threaded marshalling by implementing [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="0faf2-109">終端機可以藉由呼叫 COM API [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) ，並將 **IMarshal** 匯總至傳回的指標來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="0faf2-109">The terminal can do this by calling the COM API [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) and aggregating **IMarshal** to the returned pointer.</span></span> <span data-ttu-id="0faf2-110">終端物件的函式應該呼叫 [**IMarshal >版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="0faf2-110">The terminal object's destructor should call [**IMarshal->Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>
-   <span data-ttu-id="0faf2-111">終端機應執行或匯總任何適當的其他終端機特定介面。</span><span class="sxs-lookup"><span data-stu-id="0faf2-111">The terminal should implement or aggregate any additional terminal-specific interfaces that are appropriate.</span></span>
-   <span data-ttu-id="0faf2-112">終端機執行必須是安全線程。</span><span class="sxs-lookup"><span data-stu-id="0faf2-112">The terminal implementation must be thread-safe.</span></span>
-   <span data-ttu-id="0faf2-113">終端機執行必須 \# 針對 [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol)定義包含 Termmgr。</span><span class="sxs-lookup"><span data-stu-id="0faf2-113">The terminal implementation must \#include Termmgr.h for the definition of [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol).</span></span> <span data-ttu-id="0faf2-114">這是 Windows 2000 SP1 下的 TAPI 3 或 TAPI 3 應用程式所需的一般包含和程式庫的補充。</span><span class="sxs-lookup"><span data-stu-id="0faf2-114">This is in addition to the usual includes and libs that are needed for TAPI 3 or TAPI 3 applications under Windows 2000 SP1.</span></span>

<span data-ttu-id="0faf2-115">介面和方法的執行附注：</span><span class="sxs-lookup"><span data-stu-id="0faf2-115">Interface and method implementation notes:</span></span>

<span data-ttu-id="0faf2-116">終端機必須執行 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (雙重介面– Vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)) 。</span><span class="sxs-lookup"><span data-stu-id="0faf2-116">The terminal must implement [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (dual interface–vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).</span></span>

[<span data-ttu-id="0faf2-117">**ITTerminal：： get \_ TerminalClass**</span><span class="sxs-lookup"><span data-stu-id="0faf2-117">**ITTerminal::get\_TerminalClass**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

<span data-ttu-id="0faf2-118">終端機必須傳回您所挑選 GUID 的 **BSTR** 標記法，以識別您的終端機類型。</span><span class="sxs-lookup"><span data-stu-id="0faf2-118">The terminal must return a **BSTR** representation of a GUID you've picked that identifies your type of terminal.</span></span> <span data-ttu-id="0faf2-119">透過 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)配置 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="0faf2-119">Allocate the **BSTR** via [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span> <span data-ttu-id="0faf2-120">若要從 GUID 轉換成 **BSTR**，請呼叫 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)、 **SysAllocString** 和 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)。</span><span class="sxs-lookup"><span data-stu-id="0faf2-120">To convert from GUID to **BSTR**, call [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid), **SysAllocString**, and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

[<span data-ttu-id="0faf2-121">**ITTerminal：： get \_ TerminalType**</span><span class="sxs-lookup"><span data-stu-id="0faf2-121">**ITTerminal::get\_TerminalType**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

<span data-ttu-id="0faf2-122">如果應用程式會執行終端機，終端機通常應該會傳回 TT \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="0faf2-122">The terminal should generally return TT\_DYNAMIC if an application implements the terminal.</span></span> <span data-ttu-id="0faf2-123">傳回 TT \_ 靜態也會正常運作，如果終端機對應至硬體裝置，則傳回此值可能很適當; 不過，這麼做可能會對使用者造成混淆，因為 MSP 的靜態終端機列舉中不會有靜態終端機。</span><span class="sxs-lookup"><span data-stu-id="0faf2-123">Returning TT\_STATIC will also work, and returning this value may be appropriate if the terminal corresponds to a hardware device; however, doing this may be confusing to users because a static terminal will not be present in the MSP's static terminal enumeration.</span></span>

[<span data-ttu-id="0faf2-124">**ITTerminal：： get \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="0faf2-124">**ITTerminal::get\_State**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

<span data-ttu-id="0faf2-125">如果終端機執行不會任意限制終端機可同時連接的資料流程數目，則終端機應該一律傳回 TS \_ NOTINUSE。</span><span class="sxs-lookup"><span data-stu-id="0faf2-125">If the terminal implementation does not arbitrarily limit the number of streams that the terminal can be concurrently connected to, then the terminal should always return TS\_NOTINUSE.</span></span>

<span data-ttu-id="0faf2-126">否則，終端機執行會任意限制終端機可連接的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="0faf2-126">Otherwise, the terminal implementation arbitrarily limits the number of streams that the terminal can be connected to at a time.</span></span> <span data-ttu-id="0faf2-127">在此情況下，終端機應該會保留它所連接的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="0faf2-127">In this case, the terminal should keep a count of how many streams it is connected to.</span></span> <span data-ttu-id="0faf2-128">終端機應該在成功的 [**ITTerminalControl：： ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) 呼叫上遞增此內部計數，並在成功的 ITTerminalControl 上將它遞減 [**：:D isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0faf2-128">The terminal should increment this internal count on a successful [**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) call and decrement it on a successful [**ITTerminalControl::DisconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) call.</span></span> <span data-ttu-id="0faf2-129">在 [**ITTerminal：： get \_ 狀態**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)中， \_ 如果此計數等於可以一次選取終端機的資料流程數目上限，則應該傳回 ts INUSE; 否則，它應該會傳回 ts \_ NOTINUSE。</span><span class="sxs-lookup"><span data-stu-id="0faf2-129">In [**ITTerminal::get\_State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state), it should return TS\_INUSE if this count is equal to the maximum number of streams that the terminal can be selected on at a time; otherwise, it should return TS\_NOTINUSE.</span></span> <span data-ttu-id="0faf2-130">請注意，如果限制為1，則計數可以是布林值或終端 \_ 狀態值。</span><span class="sxs-lookup"><span data-stu-id="0faf2-130">Note that if the limit is one, the count can simply be a Boolean or a TERMINAL\_STATE value.</span></span>

[<span data-ttu-id="0faf2-131">**ITTerminal：： get \_ Name**</span><span class="sxs-lookup"><span data-stu-id="0faf2-131">**ITTerminal::get\_Name**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

<span data-ttu-id="0faf2-132">終端機會傳回其選擇的 **BSTR** 名稱，並透過 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)配置。</span><span class="sxs-lookup"><span data-stu-id="0faf2-132">The terminal should return a **BSTR** name of its choice, allocated via [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span> <span data-ttu-id="0faf2-133">此名稱對使用者應該有意義，而且應該進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="0faf2-133">This name should be meaningful to the user and should be localized.</span></span>

[<span data-ttu-id="0faf2-134">**ITTerminal：：取得 \_ 媒體媒體**</span><span class="sxs-lookup"><span data-stu-id="0faf2-134">**ITTerminal::get\_MediaType**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

<span data-ttu-id="0faf2-135">終端機應該會傳回它的媒體類型，也就是 TAPIMEDIATYPE \_ 音訊或 TAPIMEDIATYPE \_ 影片。</span><span class="sxs-lookup"><span data-stu-id="0faf2-135">The terminal should return its media type, either TAPIMEDIATYPE\_AUDIO or TAPIMEDIATYPE\_VIDEO.</span></span>

[<span data-ttu-id="0faf2-136">**ITTerminal：： get \_ 方向**</span><span class="sxs-lookup"><span data-stu-id="0faf2-136">**ITTerminal::get\_Direction**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

<span data-ttu-id="0faf2-137">終端機會傳回終端 \_ 方向列舉值，指出終端機的方向。</span><span class="sxs-lookup"><span data-stu-id="0faf2-137">The terminal returns the TERMINAL\_DIRECTION enum value indicating the direction of the terminal.</span></span> <span data-ttu-id="0faf2-138">如果終端機為雙向 (例如，橋接器) ，則必須傳回 TD \_ 雙向。</span><span class="sxs-lookup"><span data-stu-id="0faf2-138">If the terminal is bidirectional (for example, a bridge), then it must return TD\_BIDIRECTIONAL.</span></span>

<span data-ttu-id="0faf2-139">終端機必須只) 執行 [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (vtable。</span><span class="sxs-lookup"><span data-stu-id="0faf2-139">The terminal must implement [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (vtable only).</span></span>

[<span data-ttu-id="0faf2-140">**ITTerminalControl：： get \_ AddressHandle**</span><span class="sxs-lookup"><span data-stu-id="0faf2-140">**ITTerminalControl::get\_AddressHandle**</span></span>](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

<span data-ttu-id="0faf2-141">應用程式提供的終端機應該一律傳回 **Null** 作為位址控制碼。</span><span class="sxs-lookup"><span data-stu-id="0faf2-141">An application-provided terminal should always return **NULL** as the address handle.</span></span> <span data-ttu-id="0faf2-142">這會向 MSP 指出此終端機未建立在特定的 MSP 位址物件上。</span><span class="sxs-lookup"><span data-stu-id="0faf2-142">This indicates to the MSP that this terminal was not created on a specific MSP address object.</span></span>

[<span data-ttu-id="0faf2-143">**ITTerminalControl::ConnectTerminal**</span><span class="sxs-lookup"><span data-stu-id="0faf2-143">**ITTerminalControl::ConnectTerminal**</span></span>](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

<span data-ttu-id="0faf2-144">在此呼叫中，終端機會將其篩選 () 新增至指定的圖形，並將它們彼此連接（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="0faf2-144">On this call, the terminal will add its filter(s) to the given graph and connect them to each other, if applicable.</span></span> <span data-ttu-id="0faf2-145">然後，終端機會針對指定的資料流程方向，傳回終端機 (s) 所公開的 pin。</span><span class="sxs-lookup"><span data-stu-id="0faf2-145">Then the terminal should return the pin(s) exposed by the terminal for the stream direction specified.</span></span>

<span data-ttu-id="0faf2-146">不支援並行連接至多個資料流程的終端機，會 \_ 在此方法成功完成時，將內部變數設定為 TS INUSE。</span><span class="sxs-lookup"><span data-stu-id="0faf2-146">A terminal that does not support concurrent connection to multiple streams would set an internal variable to TS\_INUSE on successful completion of this method.</span></span>

<span data-ttu-id="0faf2-147">終端機可以使用此呼叫中的 *dwTerminalDirection* 參數，來判斷其所連接的資料流程方向。</span><span class="sxs-lookup"><span data-stu-id="0faf2-147">The terminal can use the *dwTerminalDirection* parameter from this call to determine the direction of the stream that it is being connected to.</span></span> <span data-ttu-id="0faf2-148">雙向終端機需要這項功能。</span><span class="sxs-lookup"><span data-stu-id="0faf2-148">This is required for bidirectional terminals.</span></span>

> [!Note]  
> <span data-ttu-id="0faf2-149">通常 (在 MSP 基類和所有已知的 Msp) 中，如果終端機從單一 [**ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) 呼叫傳回一個以上的 pin，則 msp 串流程式碼將會使連接失敗。</span><span class="sxs-lookup"><span data-stu-id="0faf2-149">Typically (in the MSP base classes and in all known MSPs), the MSP stream code will fail the connection if the terminal returns more than one pin from a single [**ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) call.</span></span> <span data-ttu-id="0faf2-150">這是很好的，因為在連線期間傳回一個以上 pin 的終端機需要 MSP 具有終端機的特殊知識，才能有效使用額外的 pin。</span><span class="sxs-lookup"><span data-stu-id="0faf2-150">This is fine, because a terminal that returns more than one pin during connection requires the MSP to have special knowledge of the terminal to make use of the extra pins effectively.</span></span>

 

[<span data-ttu-id="0faf2-151">**ITTerminalControl::CompleteConnectTerminal**</span><span class="sxs-lookup"><span data-stu-id="0faf2-151">**ITTerminalControl::CompleteConnectTerminal**</span></span>](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

<span data-ttu-id="0faf2-152">終端機應該只傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="0faf2-152">The terminal should just return S\_OK.</span></span> <span data-ttu-id="0faf2-153">終端機也可以視需要進行連線初始化。</span><span class="sxs-lookup"><span data-stu-id="0faf2-153">The terminal may also do post-connection initialization if it needs to.</span></span>

[<span data-ttu-id="0faf2-154">**ITTerminalControl：:D isconnectTerminal**</span><span class="sxs-lookup"><span data-stu-id="0faf2-154">**ITTerminalControl::DisconnectTerminal**</span></span>](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

<span data-ttu-id="0faf2-155">終端機應該進行將終端機與圖形其餘部分中斷連線所需的任何動作。</span><span class="sxs-lookup"><span data-stu-id="0faf2-155">The terminal should do whatever is needed to disconnect the terminal from the rest of the graph.</span></span> <span data-ttu-id="0faf2-156">這通常牽涉到從圖形中移除所有終端機篩選，並將終端機狀態設定為 TS \_ NOTINUSE。</span><span class="sxs-lookup"><span data-stu-id="0faf2-156">Typically this involves removing all the terminals' filters from the graph and setting the terminal state to TS\_NOTINUSE.</span></span>

[<span data-ttu-id="0faf2-157">**ITTerminalControl::RunRenderFilter**</span><span class="sxs-lookup"><span data-stu-id="0faf2-157">**ITTerminalControl::RunRenderFilter**</span></span>](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

<span data-ttu-id="0faf2-158">終端機應該只傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0faf2-158">The terminal should just return E\_NOTIMPL.</span></span>

[<span data-ttu-id="0faf2-159">**ITTerminalControl::StopRenderFilter**</span><span class="sxs-lookup"><span data-stu-id="0faf2-159">**ITTerminalControl::StopRenderFilter**</span></span>](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

<span data-ttu-id="0faf2-160">終端機應該只傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0faf2-160">The terminal should just return E\_NOTIMPL.</span></span>

 

 
