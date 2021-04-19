---
title: Windows 遠端管理詞彙
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106992245"
---
# <a name="windows-remote-management-glossary"></a><span data-ttu-id="0a676-103">Windows 遠端管理詞彙</span><span class="sxs-lookup"><span data-stu-id="0a676-103">Windows Remote Management Glossary</span></span>


<dl> <dt>

<span data-ttu-id="0a676-104">wsman： Items \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="0a676-104">\*\*\*\*wsman:Items\*\*\*\*</span></span>
</dt> <dd>

<span data-ttu-id="0a676-105">在列舉中傳回的 WS-Management protocol 元素，可取得實例和實例 [*EPRs*](/windows)。</span><span class="sxs-lookup"><span data-stu-id="0a676-105">A WS-Management protocol element returned in an enumeration that obtains both the instances and the instance [*EPRs*](/windows).</span></span> <span data-ttu-id="0a676-106">**wsman： Items** 是保存實例和其 EPR 的容器。</span><span class="sxs-lookup"><span data-stu-id="0a676-106">**wsman:Items** is a container that holds an instance and its EPR.</span></span> <span data-ttu-id="0a676-107">當要求中設定 **WSManFlagReturnObjectAndEPR** 旗標時，就會起始此類型的列舉。</span><span class="sxs-lookup"><span data-stu-id="0a676-107">This type of enumeration is initiated when the **WSManFlagReturnObjectAndEPR** flag is set in the request.</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="0a676-108">B</span><span class="sxs-lookup"><span data-stu-id="0a676-108">B</span></span>

<dl> <dt>

<span data-ttu-id="0a676-109">**基礎板管理控制器 (BMC)**</span><span class="sxs-lookup"><span data-stu-id="0a676-109">**baseboard management controller (BMC)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-110">在本機連接到伺服器的微控制器。</span><span class="sxs-lookup"><span data-stu-id="0a676-110">A microcontroller attached locally to a server.</span></span> <span data-ttu-id="0a676-111">Bmc 的感應器會監視伺服器的實體狀態，以及可透過網路通訊的個別網路連線（即使伺服器已離線）。</span><span class="sxs-lookup"><span data-stu-id="0a676-111">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="0a676-112">您可以透過 [*智慧型平臺管理介面 (IPMI)*](windows-remote-management-glossary.md) WMI 提供者來存取 BMC 資料。</span><span class="sxs-lookup"><span data-stu-id="0a676-112">You have access to BMC data through the [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-113">**基本驗證**</span><span class="sxs-lookup"><span data-stu-id="0a676-113">**Basic authentication**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-114">驗證交換中傳送的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="0a676-114">The user name and password sent in the authentication exchange.</span></span> <span data-ttu-id="0a676-115">基本驗證可以設定為在網域或工作組中使用 HTTP 或 HTTPS 傳輸。</span><span class="sxs-lookup"><span data-stu-id="0a676-115">Basic authentication can be configured to use either HTTP or HTTPS transport in a domain or workgroup.</span></span> <span data-ttu-id="0a676-116">這個方法是最不安全的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="0a676-116">This method is the least secure method of authentication.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-117">**BMC**</span><span class="sxs-lookup"><span data-stu-id="0a676-117">**BMC**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-118">請參閱 [*(BMC)*](windows-remote-management-glossary.md)的基礎板管理控制器。</span><span class="sxs-lookup"><span data-stu-id="0a676-118">See [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="0a676-119">C</span><span class="sxs-lookup"><span data-stu-id="0a676-119">C</span></span>

<dl> <dt>

<span data-ttu-id="0a676-120">**Cim**</span><span class="sxs-lookup"><span data-stu-id="0a676-120">**CIM**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-121">請參閱 [*通用訊息模型 (CIM)*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-121">See [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-122">**客戶**</span><span class="sxs-lookup"><span data-stu-id="0a676-122">**client**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-123">使用 WS-Management 通訊協定的用戶端應用程式，以存取本機或遠端電腦上的管理服務。</span><span class="sxs-lookup"><span data-stu-id="0a676-123">The client application using the WS-Management protocol to access the management service on either the local or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-124">**通用訊息模型 (CIM)**</span><span class="sxs-lookup"><span data-stu-id="0a676-124">**Common Information Model (CIM)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-125">[*分散式管理工作強制 (DMTF)*](windows-remote-management-glossary.md)模型，其描述如何代表真實世界的電腦和網路物件。</span><span class="sxs-lookup"><span data-stu-id="0a676-125">The [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md) model that describes how to represent real-world computer and network objects.</span></span> <span data-ttu-id="0a676-126">CIM 使用物件導向的開發架構，其中會使用類別和執行個體的概念來為 Managed 物件建立模型。</span><span class="sxs-lookup"><span data-stu-id="0a676-126">CIM uses an object-oriented paradigm, where managed objects are modeled using the concepts of classes and instances.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="0a676-127">D</span><span class="sxs-lookup"><span data-stu-id="0a676-127">D</span></span>

<dl> <dt>

<span data-ttu-id="0a676-128">**摘要式驗證**</span><span class="sxs-lookup"><span data-stu-id="0a676-128">**Digest authentication**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-129">一種 exchange，其中伺服器會從用戶端接收要求，並將用戶端的相關資料傳送至驗證服務器，通常是網域控制站。</span><span class="sxs-lookup"><span data-stu-id="0a676-129">An exchange wherein the server receives a request from a client and sends data about the client to an authenticating server, typically a domain controller.</span></span> <span data-ttu-id="0a676-130">如果用戶端經過驗證，則伺服器會收到摘要工作階段金鑰，用來驗證用戶端的後續要求。</span><span class="sxs-lookup"><span data-stu-id="0a676-130">If the client is authenticated, then the server receives a Digest session key used to authenticate subsequent requests from the client.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-131">**分散式管理工作強制 (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="0a676-131">**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-132">業界組織開發企業和網際網路環境的管理標準與整合技術。</span><span class="sxs-lookup"><span data-stu-id="0a676-132">The industry organization developing management standards and integration technology for enterprise and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-133">**DMTF**</span><span class="sxs-lookup"><span data-stu-id="0a676-133">**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-134">請參閱 [*分散式管理工作強制 (DMTF)*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-134">See [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="0a676-135">E</span><span class="sxs-lookup"><span data-stu-id="0a676-135">E</span></span>

<dl> <dt>

<span data-ttu-id="0a676-136">**端點**</span><span class="sxs-lookup"><span data-stu-id="0a676-136">**endpoint**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-137">[*端點參考可 (EPR)*](windows-remote-management-glossary.md)來定址的資源。</span><span class="sxs-lookup"><span data-stu-id="0a676-137">A resource that can be addressed by an [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-138">**(EPR) 的端點參考**</span><span class="sxs-lookup"><span data-stu-id="0a676-138">**endpoint reference (EPR)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-139">WS-Addressing 和 WS-Management 的組合，可同時描述 message SOAP 標頭中的資源位址。</span><span class="sxs-lookup"><span data-stu-id="0a676-139">A combination of WS-Addressing and WS-Management addressing elements that together describe an address for a resource in the message SOAP header.</span></span> <span data-ttu-id="0a676-140">這是 web 服務字詞。</span><span class="sxs-lookup"><span data-stu-id="0a676-140">This is a web service term.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-141">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="0a676-141">**enumeration**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-142">[*資源*](windows-remote-management-glossary.md)實例的集合或集合，或要求這類集合的動作。</span><span class="sxs-lookup"><span data-stu-id="0a676-142">A set, or collection, of [*resource*](windows-remote-management-glossary.md) instances or the action of requesting such a set.</span></span> <span data-ttu-id="0a676-143">在 WS-Management 通訊協定中，會使用 [*WS-列舉*](windows-remote-management-glossary.md) 來取得集合。</span><span class="sxs-lookup"><span data-stu-id="0a676-143">In WS-Management protocol, [*WS-Enumeration*](windows-remote-management-glossary.md) is used to obtain the collection.</span></span> <span data-ttu-id="0a676-144">在執行列舉的 WinRM 服務腳本時，會使用 [**Session. 列舉**](session-enumerate.md)[**和列舉值物件。**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="0a676-144">In the WinRM service scripting implementation of enumeration, [**Session.Enumerate**](session-enumerate.md) and the [**Enumerator**](enumerator.md) object are used.</span></span> <span data-ttu-id="0a676-145">對應的 c + + 方法和介面為 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) 和 [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)。</span><span class="sxs-lookup"><span data-stu-id="0a676-145">The corresponding C++ method and interface are [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) and [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-146">**EPR**</span><span class="sxs-lookup"><span data-stu-id="0a676-146">**EPR**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-147">請參閱 [*端點參考 (EPR)*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-147">See [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-148">**事件收集服務**</span><span class="sxs-lookup"><span data-stu-id="0a676-148">**Event Collection Service**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-149">從 BMC 和其他作業系統元件或應用程式接收事件的作業系統元件。</span><span class="sxs-lookup"><span data-stu-id="0a676-149">The operating system component that receives events from the BMC and other operating system components or applications.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-150">**事件轉送**</span><span class="sxs-lookup"><span data-stu-id="0a676-150">**event forwarding**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-151">遠端電腦上發生的事件通知可以傳送至訂閱應用程式。</span><span class="sxs-lookup"><span data-stu-id="0a676-151">A notification of events that occur on remote computers can be sent to subscribing applications.</span></span> <span data-ttu-id="0a676-152">事件轉送不是 WinRM 的功能，而是 [Windows 事件記錄](/windows/desktop/WES/windows-event-log)檔的功能。</span><span class="sxs-lookup"><span data-stu-id="0a676-152">Event forwarding is not a feature of WinRM, but of the [Windows Event Log](/windows/desktop/WES/windows-event-log).</span></span> <span data-ttu-id="0a676-153">在 Windows Vista 中，第一次可以使用事件轉送。</span><span class="sxs-lookup"><span data-stu-id="0a676-153">Event forwarding becomes available for the first time in Windows Vista.</span></span> <span data-ttu-id="0a676-154">管理應用程式，例如 Microsoft Operations Manager (MOM) 使用事件轉送。</span><span class="sxs-lookup"><span data-stu-id="0a676-154">The Management applications, such as Microsoft Operations Manager (MOM) use event forwarding.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="0a676-155">F</span><span class="sxs-lookup"><span data-stu-id="0a676-155">F</span></span>

<dl> <dt>

<span data-ttu-id="0a676-156">**filter**</span><span class="sxs-lookup"><span data-stu-id="0a676-156">**filter**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-157">在要求中為 [*資源*](windows-remote-management-glossary.md)指定一組有限實例的查詢機制。</span><span class="sxs-lookup"><span data-stu-id="0a676-157">A query mechanism for specifying a limited set of instances in the request for a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-158">您可以對 [**Session**](session-enumerate.md)的呼叫指定 *篩選* 參數。列舉或 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)。</span><span class="sxs-lookup"><span data-stu-id="0a676-158">You can specify a *filter* parameter on calls to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-159">**篩選方言**</span><span class="sxs-lookup"><span data-stu-id="0a676-159">**filter dialect**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-160">XML 字串，識別用來在呼叫 [**Session. 列舉**](session-enumerate.md)或 [**Iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)中指定 [*篩選*](windows-remote-management-glossary.md)的 xml 方言。</span><span class="sxs-lookup"><span data-stu-id="0a676-160">An XML string that identifies the XML dialect used to specify a [*filter*](windows-remote-management-glossary.md) in a call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span> <span data-ttu-id="0a676-161">WinRM 服務在接收要求時支援 [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) 作為篩選方言。</span><span class="sxs-lookup"><span data-stu-id="0a676-161">The WinRM service supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as a filter dialect when receiving requests.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-162">**片段**</span><span class="sxs-lookup"><span data-stu-id="0a676-162">**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-163">XML 字串，可識別資源實例的一部分，而不是整個資源。</span><span class="sxs-lookup"><span data-stu-id="0a676-163">An XML string that identifies part of an instance of a resource rather than the entire resource.</span></span> <span data-ttu-id="0a676-164">在 [**ResourceLocator**](resourcelocator.md) 物件中可找到片段支援。</span><span class="sxs-lookup"><span data-stu-id="0a676-164">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-165">**片段方言**</span><span class="sxs-lookup"><span data-stu-id="0a676-165">**fragment dialect**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-166">識別用來指定 [*片段*](windows-remote-management-glossary.md)之 xml 方言的 xml 字串。</span><span class="sxs-lookup"><span data-stu-id="0a676-166">An XML string that identifies the XML dialect used to specify a [*fragment*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-167">在 [**ResourceLocator**](resourcelocator.md) 物件中可找到片段支援。</span><span class="sxs-lookup"><span data-stu-id="0a676-167">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="0a676-168">WinRM 服務在接收要求時支援片段方言的 [*XPath*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="0a676-168">The WinRM service supports [*XPath*](windows-remote-management-glossary.md) for fragment dialect when receiving requests.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="0a676-169">I</span><span class="sxs-lookup"><span data-stu-id="0a676-169">I</span></span>

<dl> <dt>

<span data-ttu-id="0a676-170">**頻內**</span><span class="sxs-lookup"><span data-stu-id="0a676-170">**in-band**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-171">用戶端應用程式會透過 [*作業系統中的*](windows-remote-management-glossary.md) WinRM 接聽程式取得 BMC 資料。</span><span class="sxs-lookup"><span data-stu-id="0a676-171">The client application obtains BMC data through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-172">**智慧型平臺管理介面 (IPMI)**</span><span class="sxs-lookup"><span data-stu-id="0a676-172">**Intelligent Platform Management Interface (IPMI)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-173">適用于基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md)的 IT 產業標準。</span><span class="sxs-lookup"><span data-stu-id="0a676-173">An IT industry standard for the architecture of [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-174">Windows 硬體管理功能提供了一種 [*IPMI 驅動程式*](windows-remote-management-glossary.md) 和 WMI [*IPMI 提供者*](windows-remote-management-glossary.md) ，可讓管理腳本、命令列工具和應用程式取得 BMC 資料。</span><span class="sxs-lookup"><span data-stu-id="0a676-174">The Windows hardware management features supply an [*IPMI driver*](windows-remote-management-glossary.md) and a WMI [*IPMI provider*](windows-remote-management-glossary.md) that allow management scripts, command-line tools, and applications to obtain BMC data.</span></span> <span data-ttu-id="0a676-175">IPMI 提供者具有 WMI [類別](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。</span><span class="sxs-lookup"><span data-stu-id="0a676-175">The IPMI provider has WMI [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-176">**IPMI**</span><span class="sxs-lookup"><span data-stu-id="0a676-176">**IPMI**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-177">請參閱 [*智慧型平臺管理介面 (IMPI)*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-177">See [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-178">**IPMI 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="0a676-178">**IPMI driver**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-179">核心驅動程式，可讓您從作業系統元件存取基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md) 裝置。</span><span class="sxs-lookup"><span data-stu-id="0a676-179">The kernel driver that enables access to [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) devices from the operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-180">**IPMI 提供者**</span><span class="sxs-lookup"><span data-stu-id="0a676-180">**IPMI provider**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-181">標準的 WMI 提供者，定義將 [*IPMI*](windows-remote-management-glossary.md) 和其資料模型化的類別。</span><span class="sxs-lookup"><span data-stu-id="0a676-181">A standard WMI provider that defines classes modeling the [*IPMI*](windows-remote-management-glossary.md) and its data.</span></span> <span data-ttu-id="0a676-182">[IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)是從 BMC 取得資料的 COM DLL。</span><span class="sxs-lookup"><span data-stu-id="0a676-182">The [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) is a COM DLL that obtains data from the BMC.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="0a676-183">K</span><span class="sxs-lookup"><span data-stu-id="0a676-183">K</span></span>

<dl> <dt>

<span data-ttu-id="0a676-184">**KCS**</span><span class="sxs-lookup"><span data-stu-id="0a676-184">**KCS**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-185">請參閱 [*鍵盤控制器樣式 (KCS)*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-185">See [*Keyboard Controller Style (KCS)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-186">**Kerberos 驗證**</span><span class="sxs-lookup"><span data-stu-id="0a676-186">**Kerberos authentication**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-187">使用加密金鑰的用戶端和伺服器之間的相互驗證方法。</span><span class="sxs-lookup"><span data-stu-id="0a676-187">A method of mutual authentication between the client and server that uses encrypted keys.</span></span> <span data-ttu-id="0a676-188">針對在 Windows 作業系統上執行的電腦，用戶端帳戶必須是與伺服器位於相同網域的網域帳戶。</span><span class="sxs-lookup"><span data-stu-id="0a676-188">For computers running on a Windows-based operating system, the client account must be a domain account in the same domain as the server.</span></span> <span data-ttu-id="0a676-189">當用戶端使用預設認證時，如果連接字串不是下列其中一項，則 Kerberos 是驗證方法： localhost、127.0.0.1 或 \[ ：： 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="0a676-189">When a client uses default credentials, Kerberos is the authentication method if the connection string is not one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>

</dd> <dt>

<span data-ttu-id="0a676-190">**鍵盤控制器樣式 (KCS)**</span><span class="sxs-lookup"><span data-stu-id="0a676-190">**Keyboard Controller Style (KCS)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-191">[*IPMI 驅動程式*](windows-remote-management-glossary.md)用來與基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md)通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a676-191">The protocol used by the [*IPMI driver*](windows-remote-management-glossary.md) to communicate with the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="0a676-192">L</span><span class="sxs-lookup"><span data-stu-id="0a676-192">L</span></span>

<dl> <dt>

<span data-ttu-id="0a676-193">**listener**</span><span class="sxs-lookup"><span data-stu-id="0a676-193">**listener**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-194">此管理服務會執行 WS-Management 通訊協定來傳送和接收訊息。</span><span class="sxs-lookup"><span data-stu-id="0a676-194">A management service that implements WS-Management protocol to send and receive messages.</span></span> <span data-ttu-id="0a676-195">WinRM 是接聽程式服務。</span><span class="sxs-lookup"><span data-stu-id="0a676-195">WinRM is a listener service.</span></span> <span data-ttu-id="0a676-196">接聽程式是由傳輸 (HTTP 或 HTTPS) 和 IPv4 或 IPv6 位址所定義。</span><span class="sxs-lookup"><span data-stu-id="0a676-196">A listener is defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span> <span data-ttu-id="0a676-197">您可以在單一電腦上建立一個以上的 WinRM 接聽程式實例，方法是為它們提供不同的 TCP/IP 位址或埠號碼。</span><span class="sxs-lookup"><span data-stu-id="0a676-197">You can create more than one WinRM listener instance on a single computer by giving them a different TCP/IP address or port number.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="0a676-198">M</span><span class="sxs-lookup"><span data-stu-id="0a676-198">M</span></span>

<dl> <dt>

<span data-ttu-id="0a676-199">**message**</span><span class="sxs-lookup"><span data-stu-id="0a676-199">**message**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-200">在使用 [*SOAP*](windows-remote-management-glossary.md) 通訊協定所建立的電腦或個別網路之間傳輸的資訊套件。</span><span class="sxs-lookup"><span data-stu-id="0a676-200">A package of information transmitted between computers or separate networks constructed with the [*SOAP*](windows-remote-management-glossary.md) protocol.</span></span> <span data-ttu-id="0a676-201">封裝具有描述訊息目標和傳輸的標頭，以及包含訊息抵達時要使用之內容的主體。</span><span class="sxs-lookup"><span data-stu-id="0a676-201">The package has a header, that describes the message target and transport, and a body that contains the content to be used when the message arrives.</span></span> <span data-ttu-id="0a676-202">訊息是來自規格的元素組合，例如 [*ws-addressing*](windows-remote-management-glossary.md)、 [*ws-Transfer*](windows-remote-management-glossary.md)和 [*ws-management*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-202">A message is a combination of elements from specifications such as [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="0a676-203">N</span><span class="sxs-lookup"><span data-stu-id="0a676-203">N</span></span>

<dl> <dt>

<span data-ttu-id="0a676-204">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="0a676-204">**namespace**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-205">[*Wmi*](windows-remote-management-glossary.md)命名空間，這是用來控制範圍和存取的 wmi 類別和實例的邏輯群組。</span><span class="sxs-lookup"><span data-stu-id="0a676-205">A [*WMI*](windows-remote-management-glossary.md) namespace, which is a logical grouping of WMI classes and instances to control scope and access.</span></span> <span data-ttu-id="0a676-206">執行 Windows 之系統的管理資料最常見的來源是根 \\ cimv2 命名空間，其中包含 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)等類別。</span><span class="sxs-lookup"><span data-stu-id="0a676-206">The most frequent source of management data for systems running Windows is the root\\cimv2 namespace, which contains classes such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="0a676-207">例如，命名空間會出現在 WMI 類別的資源 URI 中 https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service 。</span><span class="sxs-lookup"><span data-stu-id="0a676-207">Namespaces appear in the resource URI for WMI classes, for example https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-208">**協商驗證**</span><span class="sxs-lookup"><span data-stu-id="0a676-208">**Negotiate authentication**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-209">一種經過協商、單一登入的驗證類型，也就是 [*簡單且受保護的 GSSAPI 協商機制*](windows-remote-management-glossary.md)的 Windows 實作為 (SPNEGO) 。</span><span class="sxs-lookup"><span data-stu-id="0a676-209">A negotiated, single sign on type of authentication that is the Windows implementation of [*Simple and Protected GSSAPI Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-210">SPNEGO 協商可判斷驗證是否由 Kerberos 或 NTLM 處理。</span><span class="sxs-lookup"><span data-stu-id="0a676-210">SPNEGO negotiation determines whether authentication is handled by Kerberos or NTLM.</span></span> <span data-ttu-id="0a676-211">Kerberos 是慣用的機制。</span><span class="sxs-lookup"><span data-stu-id="0a676-211">Kerberos is the preferred mechanism.</span></span> <span data-ttu-id="0a676-212">以 Windows 為基礎的系統上的 Negotiate 驗證也稱為「Windows 整合式驗證」。</span><span class="sxs-lookup"><span data-stu-id="0a676-212">Negotiate authentication on Windows-based systems is also called Windows Integrated Authentication.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-213">**數值感應器**</span><span class="sxs-lookup"><span data-stu-id="0a676-213">**numeric sensor**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-214">基礎板管理控制器中的感應器的數位類型 [*(BMC)*](windows-remote-management-glossary.md)，例如溫度或電壓。</span><span class="sxs-lookup"><span data-stu-id="0a676-214">A numeric type of sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md), for example temperature or voltage.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="0a676-215">O</span><span class="sxs-lookup"><span data-stu-id="0a676-215">O</span></span>

<dl> <dt>

<span data-ttu-id="0a676-216">**選項**</span><span class="sxs-lookup"><span data-stu-id="0a676-216">**option**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-217">資源提供者處理要求所需的其他資料。</span><span class="sxs-lookup"><span data-stu-id="0a676-217">The additional data required by the resource provider to process a request.</span></span> <span data-ttu-id="0a676-218">例如，某些 WMI 提供者需要提供其他資料做為 [**IWbemCoNtext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) 或 [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) 物件。</span><span class="sxs-lookup"><span data-stu-id="0a676-218">For example, some WMI providers require additional data supplied as [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) objects.</span></span> <span data-ttu-id="0a676-219">選項支援可在 [**ResourceLocator**](resourcelocator.md) 物件中找到。</span><span class="sxs-lookup"><span data-stu-id="0a676-219">Option support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-220">**頻外**</span><span class="sxs-lookup"><span data-stu-id="0a676-220">**out-of-band**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-221">用戶端應用程式會直接從另一部電腦的基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md) 取得資料，而不是透過作業系統中 [*的 WinRM 接聽*](windows-remote-management-glossary.md) 程式。</span><span class="sxs-lookup"><span data-stu-id="0a676-221">The client application obtains data directly from the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) of another computer, rather than through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="0a676-222">P</span><span class="sxs-lookup"><span data-stu-id="0a676-222">P</span></span>

<dl> <dt>

<span data-ttu-id="0a676-223">**拉**</span><span class="sxs-lookup"><span data-stu-id="0a676-223">**pull**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-224">系統會傳送 [*ws-列舉*](windows-remote-management-glossary.md) 提取訊息，以繼續初始呼叫 WS-列舉：列舉所啟動的列舉。</span><span class="sxs-lookup"><span data-stu-id="0a676-224">A [*WS-Enumeration*](windows-remote-management-glossary.md) pull message is sent to continue an enumeration started by an initial call to WS-Enumeration:Enumerate.</span></span> <span data-ttu-id="0a676-225">WinRM 服務中的提取作業是由列舉值 [**ReadItem**](enumerator-readitem.md) 或 [**IWSManEnumerator：： ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem)所執行。</span><span class="sxs-lookup"><span data-stu-id="0a676-225">The pull operation in the WinRM service is performed by [**Enumerator.ReadItem**](enumerator-readitem.md) or [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="0a676-226">R</span><span class="sxs-lookup"><span data-stu-id="0a676-226">R</span></span>

<dl> <dt>

<span data-ttu-id="0a676-227">**資源**</span><span class="sxs-lookup"><span data-stu-id="0a676-227">**resource**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-228">代表不同類型之管理作業或值的 [*端點*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="0a676-228">An [*endpoint*](windows-remote-management-glossary.md) that represents a distinct type of management operation or value.</span></span> <span data-ttu-id="0a676-229">服務會公開一或多個資源，而某些資源可以有一個以上的實例。</span><span class="sxs-lookup"><span data-stu-id="0a676-229">A service exposes one or more resources and some resources can have more than one instance.</span></span> <span data-ttu-id="0a676-230">管理資源類似于 WMI 類別或資料庫資料表，而實例類似于類別的實例或資料表中的資料列。</span><span class="sxs-lookup"><span data-stu-id="0a676-230">A management resource is similar to a WMI class or a database table, and an instance is similar to an instance of the class or a row in the table.</span></span> <span data-ttu-id="0a676-231">例如， [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別代表資源。</span><span class="sxs-lookup"><span data-stu-id="0a676-231">For example, the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class represents a resource.</span></span> <span data-ttu-id="0a676-232">`Win32_LogicalDisk="C:\"` 是資源的特定實例。</span><span class="sxs-lookup"><span data-stu-id="0a676-232">`Win32_LogicalDisk="C:\"` is a specific instance of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-233">**資源 URI**</span><span class="sxs-lookup"><span data-stu-id="0a676-233">**resource URI**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-234">[*統一資源識別項 (URI)*](windows-remote-management-glossary.md)用來識別系統上特定類型的資源，例如磁片或處理常式。</span><span class="sxs-lookup"><span data-stu-id="0a676-234">The [*uniform resource identifier (URI)*](windows-remote-management-glossary.md) used to identify a specific type of resource, such as disks or processes, on a system.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="0a676-235">S</span><span class="sxs-lookup"><span data-stu-id="0a676-235">S</span></span>

<dl> <dt>

<span data-ttu-id="0a676-236">**基**</span><span class="sxs-lookup"><span data-stu-id="0a676-236">**SEL**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-237">請參閱 [*) 的系統事件記錄檔 (*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-237">See [*System Event Log (SEL)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-238">**SEL 介面卡**</span><span class="sxs-lookup"><span data-stu-id="0a676-238">**SEL adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-239">將基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md) 資料傳送至 [*事件收集器*](windows-remote-management-glossary.md)的介面卡。</span><span class="sxs-lookup"><span data-stu-id="0a676-239">The adapter that sends [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) data to the [*Event Collector*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-240">**選取器**</span><span class="sxs-lookup"><span data-stu-id="0a676-240">**selector**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-241">代表 [*資源*](windows-remote-management-glossary.md)之特定實例的名稱和值組。</span><span class="sxs-lookup"><span data-stu-id="0a676-241">A name and value pair that represents a particular instance of a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-242">這基本上是識別所需資源實例的篩選準則或「金鑰」。</span><span class="sxs-lookup"><span data-stu-id="0a676-242">This is essentially a filter or "key" that identifies the desired instance of the resource.</span></span> <span data-ttu-id="0a676-243">在 [**ResourceLocator**](resourcelocator.md) 物件中找到選取器支援。</span><span class="sxs-lookup"><span data-stu-id="0a676-243">Selector support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-244">**感應器**</span><span class="sxs-lookup"><span data-stu-id="0a676-244">**sensor**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-245">基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md)的測量裝置。</span><span class="sxs-lookup"><span data-stu-id="0a676-245">A measurement device in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-246">**服務**</span><span class="sxs-lookup"><span data-stu-id="0a676-246">**service**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-247">透過 WS-Management 通訊協定和其他 [*web 服務*](windows-remote-management-glossary.md)提供管理服務給用戶端的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0a676-247">An application that provides management services to clients through the WS-Management protocol and other [*web services*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-248">服務通常會與 [*網路上的*](windows-remote-management-glossary.md) 接聽程式相同。</span><span class="sxs-lookup"><span data-stu-id="0a676-248">A service is usually the same as the [*listener*](windows-remote-management-glossary.md) on a network.</span></span> <span data-ttu-id="0a676-249">此服務具有實體傳輸位址。</span><span class="sxs-lookup"><span data-stu-id="0a676-249">The service has a physical transport address.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-250">**會話**</span><span class="sxs-lookup"><span data-stu-id="0a676-250">**session**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-251">Windows 遠端管理 [*用戶端*](windows-remote-management-glossary.md) 與本機或 [*遠端 WinRM 接聽*](windows-remote-management-glossary.md)程式或服務之間的連接。</span><span class="sxs-lookup"><span data-stu-id="0a676-251">A connection between a Windows Remote Management [*client*](windows-remote-management-glossary.md) and the local or remote WinRM [*listener*](windows-remote-management-glossary.md), or service.</span></span> <span data-ttu-id="0a676-252">此連接類似于 WMI 用戶端腳本與遠端伺服器上的 WMI 之間的連接。</span><span class="sxs-lookup"><span data-stu-id="0a676-252">This connection is similar to the connection between a WMI client script and WMI on a remote server.</span></span> <span data-ttu-id="0a676-253">會話作業（例如列舉資源 (列舉) 、取得資源的實例 (取得) ，或執行資源方法 (叫用) 是 **會話** 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="0a676-253">The session operations, such as enumerating a resource (Enumerate), getting an instance of a resource (Get), or running a resource method (Invoke) are methods of the **Session** object.</span></span> <span data-ttu-id="0a676-254">**Session** 物件是由 [**WSMan. CreateSession**](wsman-createsession.md)所建立。</span><span class="sxs-lookup"><span data-stu-id="0a676-254">A **Session** object is created by [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-255">**簡單且受保護的 GSS-API 協商機制 (SPNEGO)**</span><span class="sxs-lookup"><span data-stu-id="0a676-255">**Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-256">用戶端或伺服器在 Active Directory 內容中透過 WinRM 接收資料要求所使用的驗證機制。</span><span class="sxs-lookup"><span data-stu-id="0a676-256">An authentication mechanism used by the client or server receiving requests for data through the WinRM in an Active Directory context.</span></span> <span data-ttu-id="0a676-257">SPNEGO 是以網際網路工程任務推動力 (IETF) 所產生的 (RFC) 通訊協定為基礎。</span><span class="sxs-lookup"><span data-stu-id="0a676-257">SPNEGO is based on an Request For Comments (RFC) protocol produced by the Internet Engineering Task Force (IETF).</span></span> <span data-ttu-id="0a676-258">SPNEGO 也稱為「 [*Windows 整合式驗證*](windows-remote-management-glossary.md)」，這是 Windows 遠端管理說明主題中所使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="0a676-258">SPNEGO is also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md), the term used in the Windows Remote Management help topics.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-259">**Simple Object Access Protocol (SOAP) - 簡易物件存取通訊協定 (Simple Object Access Protocol, SOAP)**</span><span class="sxs-lookup"><span data-stu-id="0a676-259">**Simple Object Access Protocol (SOAP)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-260">Web 服務使用的 XML 架構通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a676-260">An XML-based protocol used by web services.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-261">**肥皂**</span><span class="sxs-lookup"><span data-stu-id="0a676-261">**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-262">請參閱 [*(SOAP) 的簡單物件存取通訊協定*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-262">See [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-263">**SPNEGO**</span><span class="sxs-lookup"><span data-stu-id="0a676-263">**SPNEGO**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-264">查看 [*簡單且受保護的 GSS-API 協商機制 (SPNEGO)*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-264">See [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-265">**系統事件記錄檔 (的 SEL)**</span><span class="sxs-lookup"><span data-stu-id="0a676-265">**System Event Log (SEL)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-266">基礎板管理控制器中的事件資料庫 [*(BMC)*](windows-remote-management-glossary.md) 硬體。</span><span class="sxs-lookup"><span data-stu-id="0a676-266">The database of events in the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) hardware.</span></span> <span data-ttu-id="0a676-267">「 [*SEL 介面卡*](windows-remote-management-glossary.md) 」會將這些事件傳達給作業系統。</span><span class="sxs-lookup"><span data-stu-id="0a676-267">The [*SEL adapter*](windows-remote-management-glossary.md) conveys these events to the operating system.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="0a676-268">U</span><span class="sxs-lookup"><span data-stu-id="0a676-268">U</span></span>

<dl> <dt>

<span data-ttu-id="0a676-269">**(URI 的統一資源識別項)**</span><span class="sxs-lookup"><span data-stu-id="0a676-269">**uniform resource identifier (URI)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-270">識別企業中資源的字串，例如電腦、進程、磁片磁碟機或基礎板管理控制器中的溫度感應器 [*(BMC)*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-270">A string that identifies a resource in the enterprise, such as a computer, a process, a disk drive, or a temperature sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-271">URI 是在網際網路工程任務推動小組中定義的 web 服務定址機制 (IETF) 統一資源識別項 (URI) ：一般語法 \[ RFC3986 \] 。</span><span class="sxs-lookup"><span data-stu-id="0a676-271">The URI is the web service addressing mechanism defined in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): Generic Syntax \[RFC3986\].</span></span>

</dd> <dt>

<span data-ttu-id="0a676-272">**URI**</span><span class="sxs-lookup"><span data-stu-id="0a676-272">**URI**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-273">請參閱 [*(URI) 的統一資源識別項*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-273">See [*uniform resource identifier (URI)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="0a676-274">W</span><span class="sxs-lookup"><span data-stu-id="0a676-274">W</span></span>

<dl> <dt>

<span data-ttu-id="0a676-275">**web 服務**</span><span class="sxs-lookup"><span data-stu-id="0a676-275">**web service**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-276">軟體應用程式，用於跨網際網路或網路的電腦之間的互動。</span><span class="sxs-lookup"><span data-stu-id="0a676-276">A software application used for interaction between computers across the Internet or a network.</span></span> <span data-ttu-id="0a676-277">Web 服務是由 [*Web 服務描述語言 (WSDL)*](windows-remote-management-glossary.md)所描述。</span><span class="sxs-lookup"><span data-stu-id="0a676-277">Web services are described by the [*Web Service Description Language (WSDL)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-278">Web 服務的特定描述會告知其他服務如何使用 SOAP 訊息與 web 服務互動。</span><span class="sxs-lookup"><span data-stu-id="0a676-278">The specific description of the web service tells other services how to interact with the web service by using SOAP messages.</span></span> <span data-ttu-id="0a676-279">訊息是透過傳輸（通常是 HTTP 或 HTTPS）在電腦之間傳達。</span><span class="sxs-lookup"><span data-stu-id="0a676-279">The messages are conveyed between computers by a transport, typically HTTP or HTTPS.</span></span> <span data-ttu-id="0a676-280">[*Ws-addressing*](windows-remote-management-glossary.md)、 [*ws-事件*](windows-remote-management-glossary.md)和 [*ws-management*](windows-remote-management-glossary.md) 是 web 服務應用程式用來彼此通訊的通訊協定範例。</span><span class="sxs-lookup"><span data-stu-id="0a676-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md) are examples of protocols used by web service applications to communicate with each other.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-281">**Web 服務描述語言 (WSDL)**</span><span class="sxs-lookup"><span data-stu-id="0a676-281">**Web Service Description Language (WSDL)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-282">用來定義如何與 web 服務互動的 XML 語言。</span><span class="sxs-lookup"><span data-stu-id="0a676-282">An XML-based language used to define how to interact with a web service.</span></span> <span data-ttu-id="0a676-283">WSDL 通常會描述 web 服務在傳回資料或執行作業時所需要的 SOAP 訊息。</span><span class="sxs-lookup"><span data-stu-id="0a676-283">Typically, the WSDL describes what SOAP messages the web service requires to return data or carry out operations.</span></span> <span data-ttu-id="0a676-284">只要符合 WSDL 的需求，WSDL 就能讓某個作業系統的執行與另一個作業系統上所執行的 web 服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="0a676-284">The WSDL allows an implementation from one operating system to communicate with the web service implemented on another operating system, as long as the requirements of the WSDL are met.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-285">**Windows 整合式驗證**</span><span class="sxs-lookup"><span data-stu-id="0a676-285">**Windows Integrated Authentication**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-286">請參閱 [*協商驗證*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-286">See [*Negotiate authentication*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-287">**Windows Management Instrumentation (WMI)**</span><span class="sxs-lookup"><span data-stu-id="0a676-287">**Windows Management Instrumentation (WMI)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-288">Microsoft 對 Web-Based Enterprise Management (WBEM) 標準的實施是由 [*分散式管理工作強制 (的 DMTF)*](windows-remote-management-glossary.md)所發行。</span><span class="sxs-lookup"><span data-stu-id="0a676-288">The Microsoft implementation of the Web-Based Enterprise Management (WBEM) standard published by the [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0a676-289">WMI 可讓您使用 [*通用訊息模型 (CIM)*](windows-remote-management-glossary.md) 標準的延伸模組，來管理本機和遠端電腦，並將電腦和網路物件模型。</span><span class="sxs-lookup"><span data-stu-id="0a676-289">WMI allows you to manage local and remote computers and models computer and network objects using an extension of the [*Common Information Model (CIM)*](windows-remote-management-glossary.md) standard.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-290">**Windows 遠端管理 (WinRM)**</span><span class="sxs-lookup"><span data-stu-id="0a676-290">**Windows Remote Management (WinRM)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-291">Microsoft 會根據公用標準 [*ws-management*](windows-remote-management-glossary.md) 通訊協定來實行管理 web 服務。</span><span class="sxs-lookup"><span data-stu-id="0a676-291">The Microsoft implementation of a management web service based on the public standard [*WS-Management*](windows-remote-management-glossary.md) protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-292">**Windows 遠端 Shell (WinRS)**</span><span class="sxs-lookup"><span data-stu-id="0a676-292">**Windows Remote Shell (WinRS)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-293">依賴 [*Windows 遠端管理*](windows-remote-management-glossary.md) 執行遠端命令的 shell 工具，特別是針對無周邊伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a676-293">A shell tool that relies on [*Windows Remote Management*](windows-remote-management-glossary.md) to execute remote commands, especially for headless servers.</span></span> <span data-ttu-id="0a676-294">命令列工具為 Winrs。</span><span class="sxs-lookup"><span data-stu-id="0a676-294">The command-line tool is Winrs.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-295">**WMI**</span><span class="sxs-lookup"><span data-stu-id="0a676-295">**WMI**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-296">請參閱 [*(WMI) 的 Windows Management Instrumentation*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="0a676-296">See [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a676-297">**WMI 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="0a676-297">**WMI plug-in**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-298">讓 WinRM 用戶端可以使用 WMI 資料的 WinRM 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="0a676-298">The WinRM plug-in that makes WMI data available to WinRM clients.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-299">**WS-ADDRESSING (wsa)**</span><span class="sxs-lookup"><span data-stu-id="0a676-299">**WS-Addressing (wsa)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-300">公用標準通訊協定，它是以 SOAP 為基礎的通訊協定，它會建立在網際網路上傳送的訊息標頭中使用的定址系統。</span><span class="sxs-lookup"><span data-stu-id="0a676-300">A public standard protocol, which is SOAP-based, that creates an addressing system used in the headers of messages sent across the Internet.</span></span> <span data-ttu-id="0a676-301">標準定義如何跨網路和防火牆來找出資源。</span><span class="sxs-lookup"><span data-stu-id="0a676-301">The standard defines how resources can be located across networks and firewalls.</span></span> <span data-ttu-id="0a676-302">WS-Addressing 是撰寫 WS-Management 通訊協定的其中一個 web 服務通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a676-302">WS-Addressing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-303">**Wsen) 的 WS-列舉 (**</span><span class="sxs-lookup"><span data-stu-id="0a676-303">**WS-Enumeration (wsen)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-304">公用標準通訊協定，它是以 SOAP 為基礎的，用來列舉 XML 元素序列，這些專案可能代表資料收集、記錄或其他線性資訊結構。</span><span class="sxs-lookup"><span data-stu-id="0a676-304">A public standard protocol, which is SOAP-based, for enumerating a sequence of XML elements that may represent data collections, logs, or other linear information structures.</span></span> <span data-ttu-id="0a676-305">WS-Enumeration 是撰寫 WS-Management 通訊協定的其中一個 web 服務通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a676-305">WS-Enumeration is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-306">**WS-事件 (wse)**</span><span class="sxs-lookup"><span data-stu-id="0a676-306">**WS-Eventing (wse)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-307">公用標準通訊協定（以 SOAP 為基礎），可讓一個 web 服務 (訂閱者) 訂閱和接受來自另一個 web 服務 (事件來源) 的事件通知訊息。</span><span class="sxs-lookup"><span data-stu-id="0a676-307">A public standard protocol, which is SOAP-based, that allows one web service (the subscriber) to subscribe to and accept event notification messages from another web service (the event source).</span></span> <span data-ttu-id="0a676-308">WS-Eventing 是撰寫 WS-Management 通訊協定的其中一個 web 服務通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a676-308">WS-Eventing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-309">**WS-Management**</span><span class="sxs-lookup"><span data-stu-id="0a676-309">**WS-Management**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-310">公用標準通訊協定，它是以 SOAP 為基礎的通訊協定，可在所有作業系統、電腦和裝置之間共用管理資料。</span><span class="sxs-lookup"><span data-stu-id="0a676-310">A public standard protocol, which is SOAP-based, for sharing management data among all operating systems, computers, and devices.</span></span> <span data-ttu-id="0a676-311">WinRM 用戶端或伺服器元件所傳送的所有 [*訊息*](windows-remote-management-glossary.md) 都會使用此通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a676-311">All [*messages*](windows-remote-management-glossary.md) sent by the WinRM client or server components use this protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0a676-312">**WS-傳輸 (wxf)**</span><span class="sxs-lookup"><span data-stu-id="0a676-312">**WS-Transfer (wxf)**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-313">公用標準通訊協定，它是以 SOAP 為基礎的，可透過一組簡單的動詞（例如 Get、Put、Invoke 或 Delete）來存取 web 服務型資源的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="0a676-313">A public standard protocol, which is SOAP-based, for accessing XML representations of web service-based resources through a simple set of verbs such as Get, Put, Invoke, or Delete.</span></span> <span data-ttu-id="0a676-314">WS-Transfer 定義用於傳送和接收特定資源的標記法，以及用來建立或刪除資源及其對應表示的作業。</span><span class="sxs-lookup"><span data-stu-id="0a676-314">WS-Transfer defines operations for sending and receiving the representation of a particular resource and operations for creating or deleting a resource and its corresponding representation.</span></span>

</dd> </dl>

## <a name="x"></a><span data-ttu-id="0a676-315">X</span><span class="sxs-lookup"><span data-stu-id="0a676-315">X</span></span>

<dl> <dt>

<span data-ttu-id="0a676-316">**XPath**</span><span class="sxs-lookup"><span data-stu-id="0a676-316">**XPath**</span></span>
</dt> <dd>

<span data-ttu-id="0a676-317">用來定址 XML 檔之部分的路徑標記法，類似于 URL。</span><span class="sxs-lookup"><span data-stu-id="0a676-317">A path notation for addressing parts of an XML document, similar to a URL.</span></span> <span data-ttu-id="0a676-318">XPath 運算式是要從 XML 檔中的目前位置取得至另一個節點或一組節點的片語序列。</span><span class="sxs-lookup"><span data-stu-id="0a676-318">An XPath expression is a sequence of phrases to get from the current location in the XML document to another node or set of nodes.</span></span> <span data-ttu-id="0a676-319">片語會以正斜線分隔 ( "/" ) 個字元。</span><span class="sxs-lookup"><span data-stu-id="0a676-319">The phrases are separated by forward-slash ("/") characters.</span></span> <span data-ttu-id="0a676-320">WinRM 服務支援 [*片段方言*](windows-remote-management-glossary.md)的 [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) 。</span><span class="sxs-lookup"><span data-stu-id="0a676-320">The WinRM service supports [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) for [*fragment dialect*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

 

 