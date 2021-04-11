---
description: WMI 包含一組類別，可針對使用 WMI 提供者的用戶端應用程式進行疑難排解。
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: 疑難排解 WMI 用戶端應用程式
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193860"
---
# <a name="troubleshooting-wmi-client-applications"></a><span data-ttu-id="6f4eb-103">疑難排解 WMI 用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="6f4eb-103">Troubleshooting WMI Client Applications</span></span>

<span data-ttu-id="6f4eb-104">WMI 包含一組類別，可針對使用 WMI 提供者的用戶端應用程式 [進行疑難排解](wmi-troubleshooting-classes.md) 。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-104">WMI contains a set of classes for [troubleshooting](wmi-troubleshooting-classes.md) client applications that use WMI providers.</span></span> <span data-ttu-id="6f4eb-105">疑難排解事件類別結合了 WMI 事件類別，讓您可以使用已捕捉的疑難排解事件記錄檔來追蹤應用程式的執行。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-105">The troubleshooting event classes are coupled to WMI event classes, such that you can track your application execution using a log of captured troubleshooting events.</span></span>

<span data-ttu-id="6f4eb-106">下列清單包含疑難排解事件類別的範例：</span><span class="sxs-lookup"><span data-stu-id="6f4eb-106">The following list contains examples of troubleshooting event classes:</span></span>

-   [<span data-ttu-id="6f4eb-107">**Msft \_ 的 wmiprovider \_ ExecMethodAsyncEvent \_ 預先**</span><span class="sxs-lookup"><span data-stu-id="6f4eb-107">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Pre**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    <span data-ttu-id="6f4eb-108">在 WMI 對提供者呼叫 [**IWbemServices：： ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) 之前引發。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-108">Raised before WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

-   [<span data-ttu-id="6f4eb-109">**Msft \_ 的 wmiprovider \_ ExecMethodAsyncEvent \_ 文章**</span><span class="sxs-lookup"><span data-stu-id="6f4eb-109">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Post**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    <span data-ttu-id="6f4eb-110">在 WMI 呼叫提供者上的 [**IWbemServices：： ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) 之後引發。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-110">Raised after WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

<span data-ttu-id="6f4eb-111">下列程式顯示如何針對應用程式執行進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-111">The following procedure shows how to troubleshoot application execution.</span></span>

<span data-ttu-id="6f4eb-112">**設定 WMI 疑難排解**</span><span class="sxs-lookup"><span data-stu-id="6f4eb-112">**To set up WMI troubleshooting**</span></span>

1.  <span data-ttu-id="6f4eb-113">建立並編譯 MOF 檔案，以使用 WMI 記錄事件取用者。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-113">Create and compile a MOF file to use the WMI logging event consumer.</span></span>
2.  <span data-ttu-id="6f4eb-114">執行您的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-114">Run your client application.</span></span>
3.  <span data-ttu-id="6f4eb-115">查看所有提供者作業和失敗事件的疑難排解記錄檔，並分析記錄以診斷您遇到的用戶端問題。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-115">View the troubleshooting log file for all provider operation and failure events, and analyze the log to diagnose the client problems you are encountering.</span></span>

<span data-ttu-id="6f4eb-116">另一個疑難排解方法是在 **根 \\ cimv2** 命名空間中列舉 [**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)，以查看目前在電腦快取中的提供者清單。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-116">Another troubleshooting approach is to view the list of providers currently in the computer cache, by enumerating [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="6f4eb-117">此類別中有一些方法，可讓您載入和卸載提供者以進行偵錯工具或安裝。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-117">There are methods in this class that enable you to load and unload providers for debugging or setup purposes.</span></span>

<span data-ttu-id="6f4eb-118">下列程式碼範例會使用 WMI 記錄事件取用者來捕捉父事件類別的所有事件，進而捕捉所有提供者作業事件。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-118">The following code example uses the WMI logging event consumer to capture all events of the parent event class, thus capturing all provider operation events.</span></span>

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

<span data-ttu-id="6f4eb-119">當錯誤訊息表示提供者載入失敗時，請使用 [**MSFT \_ 的 wmiprovider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) 來識別造成錯誤的提供者。</span><span class="sxs-lookup"><span data-stu-id="6f4eb-119">When error messages indicate provider load failure, use [**MSFT\_WmiProvider\_LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) to identify which provider caused the fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f4eb-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f4eb-120">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6f4eb-121">[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="6f4eb-121">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="6f4eb-122">WMI 疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="6f4eb-122">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
