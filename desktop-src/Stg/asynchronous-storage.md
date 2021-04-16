---
title: 非同步存放裝置
description: 非同步存放裝置可增強 COM 結構化儲存規格，以支援在高延遲的低速連結網路（例如網際網路）上非同步下載儲存物件。
ms.assetid: 12b97059-2c8c-4712-8a76-03c3ce7094a0
keywords:
- 結構化儲存體 Strctd Stg.，非同步儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dd1d739223fb07c72de6c63ee173c316a132e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463484"
---
# <a name="asynchronous-storage"></a><span data-ttu-id="36f27-104">非同步存放裝置</span><span class="sxs-lookup"><span data-stu-id="36f27-104">Asynchronous Storage</span></span>

<span data-ttu-id="36f27-105">非同步存放裝置可增強 COM 結構化儲存規格，以支援在高延遲的低速連結網路（例如網際網路）上非同步下載儲存物件。</span><span class="sxs-lookup"><span data-stu-id="36f27-105">Asynchronous storage enhances the COM structured storage specification to support asynchronous download of storage objects on high-latency, slow-link networks such as the Internet.</span></span> <span data-ttu-id="36f27-106">非同步存儲可讓使用複合檔案的新舊應用程式，在透過現有的網際網路通訊協定存取時有效地轉譯其內容。</span><span class="sxs-lookup"><span data-stu-id="36f27-106">Asynchronous storage enables both new and legacy applications that use compound files to efficiently render their content when accessed by means of existing Internet protocols.</span></span> <span data-ttu-id="36f27-107">對 World Wide Web 服務器的單一要求會觸發網頁內所包含的嵌套物件下載，而不需要個別要求每個物件。</span><span class="sxs-lookup"><span data-stu-id="36f27-107">A single request to a World Wide Web server triggers the download of nested objects contained within a Web page, eliminating the need to separately request each object.</span></span> <span data-ttu-id="36f27-108">非同步下載和存取機制可讓應用程式在收到所有資料之前，轉譯第一頁的資料。</span><span class="sxs-lookup"><span data-stu-id="36f27-108">An asynchronous download and access mechanism enables an application to render the first page of data before all the data has been received.</span></span> <span data-ttu-id="36f27-109">Web 發行者可以指定頁面元素的確切順序，而不會相依于網路拓朴和伺服器可用性的隨機因素。</span><span class="sxs-lookup"><span data-stu-id="36f27-109">The exact order in which elements of a page become available can be specified by the Web publisher and is not dependent on random factors of network topology and server availability.</span></span>

<span data-ttu-id="36f27-110">非同步存放裝置可與非同步名字區一起運作，以提供完整的非同步系結行為。</span><span class="sxs-lookup"><span data-stu-id="36f27-110">Asynchronous storage works together with asynchronous monikers to provide complete asynchronous binding behavior.</span></span> <span data-ttu-id="36f27-111">如需非同步名字組的詳細資訊，請參閱 Microsoft ActiveX 軟體發展工具組。</span><span class="sxs-lookup"><span data-stu-id="36f27-111">For more information about asynchronous monikers, see the Microsoft ActiveX software development kit.</span></span> <span data-ttu-id="36f27-112">通訊協定特定的非同步標記會觸發系結作業，並設定必要的元件。</span><span class="sxs-lookup"><span data-stu-id="36f27-112">A protocol-specific asynchronous moniker triggers the binding operation and sets up the required components.</span></span> <span data-ttu-id="36f27-113">在網際網路案例中，此標記可以剖析 URL 以系結至物件或儲存體。</span><span class="sxs-lookup"><span data-stu-id="36f27-113">In the Internet case, this moniker would be one that can parse a URL to bind to an object or storage.</span></span> <span data-ttu-id="36f27-114">如果系結作業的目標是持續性物件，則呼叫 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) 會傳回非同步儲存物件。</span><span class="sxs-lookup"><span data-stu-id="36f27-114">If the target of the binding operation is a persistent object, the call to [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) returns an asynchronous storage object.</span></span>

> [!Note]  
> <span data-ttu-id="36f27-115">Microsoft URL 名字標記的目前版本不支援非同步存放裝置。</span><span class="sxs-lookup"><span data-stu-id="36f27-115">The current version of Microsoft URL monikers does not support asynchronous storage.</span></span>

 

<span data-ttu-id="36f27-116">非同步標記用戶端會藉由執行系結狀態回呼物件，並向系結內容註冊來要求非同步系結。</span><span class="sxs-lookup"><span data-stu-id="36f27-116">An asynchronous moniker client requests asynchronous binding by implementing a bind-status callback object and registering it with the bind context.</span></span> <span data-ttu-id="36f27-117">系結狀態回呼物件會公開 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面，此介面可讓用戶端指定系結喜好設定，並在系結作業過程中接收進度和全域資料可用性通知。</span><span class="sxs-lookup"><span data-stu-id="36f27-117">The bind-status callback object exposes the [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interface, which enables the client to specify binding preferences and to receive progress and global data-availability notifications during the course of a binding operation.</span></span> <span data-ttu-id="36f27-118">非同步複合檔案執行提供 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify)的連接點，用戶端可以使用此連接點來接收個別資料流程的特定可用性通知。</span><span class="sxs-lookup"><span data-stu-id="36f27-118">The asynchronous compound file implementation provides a connection point for [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify), which clients can use to receive specific availability notifications on individual streams.</span></span>

 

 