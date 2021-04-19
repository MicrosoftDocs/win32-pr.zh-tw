---
description: 佇列的標記是用來以程式設計的方式啟用已排入佇列的元件。
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: 使用佇列的標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973583"
---
# <a name="using-the-queue-moniker"></a><span data-ttu-id="a294e-103">使用佇列的標記</span><span class="sxs-lookup"><span data-stu-id="a294e-103">Using the Queue Moniker</span></span>

<span data-ttu-id="a294e-104">佇列的標記是用來以程式設計的方式啟用已排入佇列的元件。</span><span class="sxs-lookup"><span data-stu-id="a294e-104">The queue moniker is used to activate a queued component programmatically.</span></span> <span data-ttu-id="a294e-105">佇列的標記需要它收到類別識別碼， (要從其右邊的新的標記叫用之物件的 CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="a294e-105">The queue moniker requires that it receive the class ID (CLSID) of the object to be invoked from the new moniker directly to the right of it.</span></span> <span data-ttu-id="a294e-106">當保留在前面時，新的標記會將 CLSID 傳遞給它左邊的標記。</span><span class="sxs-lookup"><span data-stu-id="a294e-106">When left-prefixed, the new moniker passes the CLSID to the moniker to the left of it.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="a294e-107">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="a294e-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="a294e-108">不適用。</span><span class="sxs-lookup"><span data-stu-id="a294e-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="a294e-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a294e-109">Visual Basic</span></span>

<span data-ttu-id="a294e-110">GetObject 顯示名稱參數為 "queue：/new："，後面接著程式識別碼或字串形式 GUID （包含或不含大括弧），而伺服器物件要具現化。</span><span class="sxs-lookup"><span data-stu-id="a294e-110">The GetObject display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="a294e-111">下列範例顯示具有佇列名字標記之元件的三個有效啟用：</span><span class="sxs-lookup"><span data-stu-id="a294e-111">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a><span data-ttu-id="a294e-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="a294e-112">C/C++</span></span>

<span data-ttu-id="a294e-113">[**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject)顯示名稱參數為 "queue：/new："，後面接著程式識別碼或字串形式 GUID （包含或不含大括弧），以具現化的伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="a294e-113">The [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="a294e-114">下列範例顯示具有佇列名字標記之元件的三個有效啟用：</span><span class="sxs-lookup"><span data-stu-id="a294e-114">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a><span data-ttu-id="a294e-115">備註</span><span class="sxs-lookup"><span data-stu-id="a294e-115">Remarks</span></span>

<span data-ttu-id="a294e-116">佇列的標記會接受選擇性參數，以修改傳送至訊息佇列的訊息屬性。</span><span class="sxs-lookup"><span data-stu-id="a294e-116">The queue moniker accepts optional parameters that alter the properties of the message sent to Message Queuing.</span></span> <span data-ttu-id="a294e-117">例如，若要讓訊息佇列的訊息以優先權6傳送，已排入佇列的元件將會依照下列方式啟用：</span><span class="sxs-lookup"><span data-stu-id="a294e-117">For example, to cause the Message Queuing message to be sent with a priority 6, the queued component would be activated as follows:</span></span>

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

<span data-ttu-id="a294e-118">下表列出會影響目的地佇列的佇列名字標記參數。</span><span class="sxs-lookup"><span data-stu-id="a294e-118">The following table lists the queue moniker parameters that affect the destination queue.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a294e-119">參數</span><span class="sxs-lookup"><span data-stu-id="a294e-119">Parameter</span></span></th>
<th><span data-ttu-id="a294e-120">Description</span><span class="sxs-lookup"><span data-stu-id="a294e-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a294e-121"><em>ComputerName</em></span><span class="sxs-lookup"><span data-stu-id="a294e-121"><em>ComputerName</em></span></span><br/></td>
<td><span data-ttu-id="a294e-122">指定訊息佇列佇列路徑名稱的電腦名稱稱部分。</span><span class="sxs-lookup"><span data-stu-id="a294e-122">Specifies the computer name portion of a Message Queuing queue path name.</span></span> <span data-ttu-id="a294e-123">訊息佇列的佇列路徑名稱會格式化為<em>ComputerName</em> \ <em>QueueName</em>。</span><span class="sxs-lookup"><span data-stu-id="a294e-123">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="a294e-124">如果未指定，則會使用與已設定之應用程式相關聯的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a294e-124">If not specified, the computer name associated with the configured application is used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-125"><em>QueueName</em></span><span class="sxs-lookup"><span data-stu-id="a294e-125"><em>QueueName</em></span></span><br/></td>
<td><span data-ttu-id="a294e-126">指定訊息佇列的佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="a294e-126">Specifies the Message Queuing queue name.</span></span> <span data-ttu-id="a294e-127">訊息佇列的佇列路徑名稱會格式化為<em>ComputerName</em> \ <em>QueueName</em>。</span><span class="sxs-lookup"><span data-stu-id="a294e-127">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="a294e-128">如果未指定，則會使用與已設定之應用程式相關聯的佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="a294e-128">If not specified, the queue name associated with the configured application is used.</span></span><br/> <span data-ttu-id="a294e-129">若要取得非交易式佇列，您可以先指定佇列名稱，然後建立相同名稱的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a294e-129">To get a non-transactional queue, you can specify the queue name first and then create a COM+ application of the same name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a294e-130"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="a294e-130"><em>PathName</em></span></span><br/></td>
<td><span data-ttu-id="a294e-131">指定完整訊息佇列的佇列路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="a294e-131">Specifies the complete Message Queuing queue path name.</span></span> <span data-ttu-id="a294e-132">如果未指定，則會使用與已設定之應用程式相關聯的訊息佇列佇列路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="a294e-132">If not specified, the Message Queuing queue path name associated with the configured application is used.</span></span> <span data-ttu-id="a294e-133">若要覆寫目的地名稱，可為訊息佇列工作組安裝指定下列格式的路徑：</span><span class="sxs-lookup"><span data-stu-id="a294e-133">To override the destination name, the path can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="a294e-134">Queue：<em>PathName</em> = <em>ComputerName</em>\PRI加值稅E $ \ AppName/new： Myproject. CMyClass</span><span class="sxs-lookup"><span data-stu-id="a294e-134">Queue:<em>PathName</em>=<em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a294e-135">C 和 Microsoft Visual C++ 程式設計語言都需要兩個反斜線，以表示字串常值中的一個反斜線，例如芝加哥 \\ 薪資。</span><span class="sxs-lookup"><span data-stu-id="a294e-135">Both the C and Microsoft Visual C++ programming languages require two backslashes to represent one backslash within string literals for example, chicago\\payroll.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-136"><em>Msmq.formatname</em></span><span class="sxs-lookup"><span data-stu-id="a294e-136"><em>FormatName</em></span></span><br/></td>
<td><span data-ttu-id="a294e-137">當您將 COM + 應用程式標示為已排入佇列時，COM + 會建立其名稱與應用程式相同的訊息佇列佇列。</span><span class="sxs-lookup"><span data-stu-id="a294e-137">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="a294e-138">該佇列的訊息佇列格式名稱位於與 COM + 應用程式相關聯的 COM + 目錄中。</span><span class="sxs-lookup"><span data-stu-id="a294e-138">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="a294e-139">若要覆寫目的地名稱，可為訊息佇列工作組安裝指定下列格式的格式名稱：</span><span class="sxs-lookup"><span data-stu-id="a294e-139">To override the destination name, the format name can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="a294e-140">Queue：<em>msmq.formatname</em>= DIRECT = OS：<em>ComputerName</em>\PRI加值稅E $ \ AppName/new： ProgId</span><span class="sxs-lookup"><span data-stu-id="a294e-140">Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId</span></span><br/> <span data-ttu-id="a294e-141">在 Active Directory 設定中， &quot; &quot; 不會將私用 $ 指定為佇列名稱的一部分。</span><span class="sxs-lookup"><span data-stu-id="a294e-141">In an Active Directory configuration, &quot;PRIVATE$&quot; is not specified as part of the queue name.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="a294e-142">選擇性的佇列名字標記參數是由左至右處理。</span><span class="sxs-lookup"><span data-stu-id="a294e-142">Optional queue moniker parameters are processed left-to-right.</span></span> <span data-ttu-id="a294e-143">請只指定每個關鍵字一次。</span><span class="sxs-lookup"><span data-stu-id="a294e-143">Specify each keyword only one time.</span></span> <span data-ttu-id="a294e-144">指定 *PathName* 參數會取代 *ComputerName* 和 *QueueName* 參數。</span><span class="sxs-lookup"><span data-stu-id="a294e-144">Specifying the *PathName* parameter replaces both the *ComputerName* and *QueueName* parameters.</span></span> <span data-ttu-id="a294e-145">特定的 *msmq.formatname* 參數會先刪除 *ComputerName*、 *QueueName* 和 *PathName* 參數的知識。</span><span class="sxs-lookup"><span data-stu-id="a294e-145">A specific *FormatName* parameter deletes prior knowledge of a *ComputerName*, *QueueName*, and *PathName* parameter.</span></span>

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a><span data-ttu-id="a294e-146">將佇列元件接聽程式與特定私用佇列產生關聯</span><span class="sxs-lookup"><span data-stu-id="a294e-146">Associating the Queued Components Listener with a Specific Private Queue</span></span>

<span data-ttu-id="a294e-147">COM + 佇列的元件接聽程式只能從與標示為已排入佇列的 COM + 應用程式相關聯的佇列接收</span><span class="sxs-lookup"><span data-stu-id="a294e-147">The COM+ Queued Components listener receives only from queues associated with the COM+ application marked queued.</span></span> <span data-ttu-id="a294e-148">當您將 COM + 應用程式標示為已排入佇列時，COM + 會建立其名稱與應用程式相同的訊息佇列佇列。</span><span class="sxs-lookup"><span data-stu-id="a294e-148">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="a294e-149">該佇列的訊息佇列格式名稱位於與 COM + 應用程式相關聯的 COM + 目錄中。</span><span class="sxs-lookup"><span data-stu-id="a294e-149">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="a294e-150">當 COM + 應用程式啟動並標示為接聽時，會啟動 COM + 應用程式進程中的接聽程式，並開啟佇列。</span><span class="sxs-lookup"><span data-stu-id="a294e-150">When the COM+ application is started and marked as listen, a listener in the COM+ application process is started and the queue is opened.</span></span> <span data-ttu-id="a294e-151">下表列出會影響訊息佇列訊息的佇列名字標記參數。</span><span class="sxs-lookup"><span data-stu-id="a294e-151">The following table lists the queue moniker parameters that affect the Message Queuing message.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a294e-152">參數</span><span class="sxs-lookup"><span data-stu-id="a294e-152">Parameter</span></span></th>
<th><span data-ttu-id="a294e-153">Description</span><span class="sxs-lookup"><span data-stu-id="a294e-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a294e-154"><em>AppSpecific</em></span><span class="sxs-lookup"><span data-stu-id="a294e-154"><em>AppSpecific</em></span></span><br/></td>
<td><span data-ttu-id="a294e-155">指定不帶正負號的整數，例如 AppSpecific = 12345。</span><span class="sxs-lookup"><span data-stu-id="a294e-155">Specifies an unsigned integer for example, AppSpecific=12345.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-156"><em>AuthLevel</em></span><span class="sxs-lookup"><span data-stu-id="a294e-156"><em>AuthLevel</em></span></span><br/></td>
<td><span data-ttu-id="a294e-157">指定訊息驗證層級。</span><span class="sxs-lookup"><span data-stu-id="a294e-157">Specifies the message authentication level.</span></span> <span data-ttu-id="a294e-158">已驗證的訊息會經過數位簽署，而且需要憑證給傳送訊息的使用者。</span><span class="sxs-lookup"><span data-stu-id="a294e-158">An authenticated message is digitally signed and requires a certificate for the user sending the message.</span></span> <span data-ttu-id="a294e-159">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-159">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-160">MQMSG_AUTH_LEVEL_NONE，0</span><span class="sxs-lookup"><span data-stu-id="a294e-160">MQMSG_AUTH_LEVEL_NONE,0</span></span></li>
<li><span data-ttu-id="a294e-161">MQMSG_AUTH_LEVEL_ALWAYS，1</span><span class="sxs-lookup"><span data-stu-id="a294e-161">MQMSG_AUTH_LEVEL_ALWAYS,1</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a294e-162"><em>傳遞</em></span><span class="sxs-lookup"><span data-stu-id="a294e-162"><em>Delivery</em></span></span><br/></td>
<td><span data-ttu-id="a294e-163">指定訊息傳遞選項。</span><span class="sxs-lookup"><span data-stu-id="a294e-163">Specifies the message delivery option.</span></span> <span data-ttu-id="a294e-164">交易式佇列會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="a294e-164">This value is ignored for transactional queues.</span></span> <span data-ttu-id="a294e-165">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-165">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-166">MQMSG_DELIVERY_EXPRESS，0</span><span class="sxs-lookup"><span data-stu-id="a294e-166">MQMSG_DELIVERY_EXPRESS,0</span></span></li>
<li><span data-ttu-id="a294e-167">MQMSG_DELIVERY_RECOVERABLE，1</span><span class="sxs-lookup"><span data-stu-id="a294e-167">MQMSG_DELIVERY_RECOVERABLE,1</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-168"><em>EncryptAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="a294e-168"><em>EncryptAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="a294e-169">指定訊息佇列用來加密和解密訊息的加密演算法。</span><span class="sxs-lookup"><span data-stu-id="a294e-169">Specifies the encryption algorithm to be used by Message Queuing to encrypt and decrypt the message.</span></span> <span data-ttu-id="a294e-170">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-170">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-171">CALG_RC2，CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="a294e-171">CALG_RC2, CALG_RC4</span></span></li>
<li><span data-ttu-id="a294e-172"><em>EncryptAlgorithm</em>訊息佇列可以接受的任何整數值。</span><span class="sxs-lookup"><span data-stu-id="a294e-172">Any integer value that is acceptable to Message Queuing for an <em>EncryptAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a294e-173"><em>HashAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="a294e-173"><em>HashAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="a294e-174">指定密碼編譯雜湊函數。</span><span class="sxs-lookup"><span data-stu-id="a294e-174">Specifies a cryptographic hash function.</span></span> <span data-ttu-id="a294e-175">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-175">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-176">CALG_MD2，CALG_MD4，CALG_MD5，CALG_SHA，CALG_SHA1，CALG_MAC，CALG_SSL3_SHAMD5，CALG_HMAC，CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="a294e-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span></span></li>
<li><span data-ttu-id="a294e-177"><em>HashAlgorithm</em>訊息佇列可以接受的任何整數值。</span><span class="sxs-lookup"><span data-stu-id="a294e-177">Any integer value that is acceptable to Message Queuing for a <em>HashAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-178">日誌</span><span class="sxs-lookup"><span data-stu-id="a294e-178">Journal</span></span><br/></td>
<td><span data-ttu-id="a294e-179">指定訊息佇列的訊息日誌選項。</span><span class="sxs-lookup"><span data-stu-id="a294e-179">Specifies the Message Queuing message journal option.</span></span> <span data-ttu-id="a294e-180">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-180">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-181">MQMSG_JOURNAL_NONE，0</span><span class="sxs-lookup"><span data-stu-id="a294e-181">MQMSG_JOURNAL_NONE,0</span></span></li>
<li><span data-ttu-id="a294e-182">MQMSG_DEADLETTER，1</span><span class="sxs-lookup"><span data-stu-id="a294e-182">MQMSG_DEADLETTER,1</span></span></li>
<li><span data-ttu-id="a294e-183">MQMSG_JOURNAL，2</span><span class="sxs-lookup"><span data-stu-id="a294e-183">MQMSG_JOURNAL,2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a294e-184"><em>標籤</em></span><span class="sxs-lookup"><span data-stu-id="a294e-184"><em>Label</em></span></span><br/></td>
<td><span data-ttu-id="a294e-185">指定最多 MQ_MAX_MSG_LABEL_LEN 個字元的訊息標籤字串。</span><span class="sxs-lookup"><span data-stu-id="a294e-185">Specifies a message label string up to MQ_MAX_MSG_LABEL_LEN characters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-186"><em>MaxTimeToReachQueue</em></span><span class="sxs-lookup"><span data-stu-id="a294e-186"><em>MaxTimeToReachQueue</em></span></span><br/></td>
<td><span data-ttu-id="a294e-187">指定訊息抵達佇列的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a294e-187">Specifies a maximum time, in seconds, for the message to reach the queue.</span></span> <br/> <span data-ttu-id="a294e-188">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-188">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-189">INFINITE</span><span class="sxs-lookup"><span data-stu-id="a294e-189">INFINITE</span></span></li>
<li><span data-ttu-id="a294e-190">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="a294e-190">LONG_LIVED</span></span></li>
<li><span data-ttu-id="a294e-191">秒數</span><span class="sxs-lookup"><span data-stu-id="a294e-191">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a294e-192"><em>MaxTimeToReceive</em></span><span class="sxs-lookup"><span data-stu-id="a294e-192"><em>MaxTimeToReceive</em></span></span><br/></td>
<td><span data-ttu-id="a294e-193">指定目標應用程式接收訊息的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a294e-193">Specifies a maximum time, in seconds, for the message to be received by the target application.</span></span> <span data-ttu-id="a294e-194">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-194">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-195">INFINITE</span><span class="sxs-lookup"><span data-stu-id="a294e-195">INFINITE</span></span></li>
<li><span data-ttu-id="a294e-196">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="a294e-196">LONG_LIVED</span></span></li>
<li><span data-ttu-id="a294e-197">秒數</span><span class="sxs-lookup"><span data-stu-id="a294e-197">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-198"><em>優先順序</em></span><span class="sxs-lookup"><span data-stu-id="a294e-198"><em>Priority</em></span></span><br/></td>
<td><span data-ttu-id="a294e-199">指定允許的訊息佇列值內的訊息優先權層級。</span><span class="sxs-lookup"><span data-stu-id="a294e-199">Specifies a message priority level, within the Message Queuing values permitted.</span></span><br/> <span data-ttu-id="a294e-200">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-200">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-201">MQ_MIN_PRIORITY，0</span><span class="sxs-lookup"><span data-stu-id="a294e-201">MQ_MIN_PRIORITY,0</span></span></li>
<li><span data-ttu-id="a294e-202">MQ_MAX_PRIORITY，7</span><span class="sxs-lookup"><span data-stu-id="a294e-202">MQ_MAX_PRIORITY,7</span></span></li>
<li><span data-ttu-id="a294e-203">MQ_DEFAULT_PRIORITY，3</span><span class="sxs-lookup"><span data-stu-id="a294e-203">MQ_DEFAULT_PRIORITY,3</span></span></li>
<li><span data-ttu-id="a294e-204">介於0和7之間的數位</span><span class="sxs-lookup"><span data-stu-id="a294e-204">Number between 0 and 7</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a294e-205"><em>PrivLevel</em></span><span class="sxs-lookup"><span data-stu-id="a294e-205"><em>PrivLevel</em></span></span><br/></td>
<td><span data-ttu-id="a294e-206">指定用來加密訊息的隱私權等級。</span><span class="sxs-lookup"><span data-stu-id="a294e-206">Specifies a privacy level, used to encrypt messages.</span></span><br/> <span data-ttu-id="a294e-207">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-207">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-208">MQMSG_PRIV_LEVEL_NONE、無、0</span><span class="sxs-lookup"><span data-stu-id="a294e-208">MQMSG_PRIV_LEVEL_NONE, NONE, 0</span></span></li>
<li><span data-ttu-id="a294e-209">MQMSG_PRIV_LEVEL_BODY，主體，</span><span class="sxs-lookup"><span data-stu-id="a294e-209">MQMSG_PRIV_LEVEL_BODY, BODY,</span></span></li>
<li><span data-ttu-id="a294e-210">MQMSG_PRIV_LEVEL_BODY_BASE，BODY_BASE，1</span><span class="sxs-lookup"><span data-stu-id="a294e-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span></span></li>
<li><span data-ttu-id="a294e-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED、BODY_ENHANCED、3</span><span class="sxs-lookup"><span data-stu-id="a294e-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a294e-212"><em>追蹤</em></span><span class="sxs-lookup"><span data-stu-id="a294e-212"><em>Trace</em></span></span><br/></td>
<td><span data-ttu-id="a294e-213">指定追蹤訊息佇列路由中使用的追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="a294e-213">Specifies trace options, used in tracing Message Queuing routing.</span></span><br/> <span data-ttu-id="a294e-214">可接受的值：</span><span class="sxs-lookup"><span data-stu-id="a294e-214">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="a294e-215">MQMSG_TRACE_NONE，0</span><span class="sxs-lookup"><span data-stu-id="a294e-215">MQMSG_TRACE_NONE,0</span></span></li>
<li><span data-ttu-id="a294e-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE，1</span><span class="sxs-lookup"><span data-stu-id="a294e-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a294e-217">您可以使用 COM 物件來取得一組完整的 COM + 系統管理 SDK 函數。</span><span class="sxs-lookup"><span data-stu-id="a294e-217">The complete set of COM+ Administrative SDK functions is available by using COM objects.</span></span> <span data-ttu-id="a294e-218">這可讓任何程式視需要啟動和停止 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a294e-218">This allows any program to start and stop COM+ applications as required.</span></span>

> [!Note]  
> <span data-ttu-id="a294e-219">當 COM + 應用程式啟動時，它是正在執行的應用程式，而不是應用程式內的個別元件。</span><span class="sxs-lookup"><span data-stu-id="a294e-219">When a COM+ application is started, it is the application that is running, not the individual components within the application.</span></span> <span data-ttu-id="a294e-220">如果應用程式呼叫未排入佇列的元件，則會啟動包含元件的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a294e-220">If an application calls a non-queued component, the COM+ application that contains the component is started.</span></span> <span data-ttu-id="a294e-221">如果已啟用 [接聽程式] 核取方塊，接聽程式也會啟動，並開始處理已排入佇列之元件的訊息。</span><span class="sxs-lookup"><span data-stu-id="a294e-221">If the listener check box is enabled, the listener also starts and begins processing for messages for queued components.</span></span> <span data-ttu-id="a294e-222">雖然已排入佇列的元件服務可以透過這種方式來啟動，但如果您將已排入佇列和未排入佇列的元件封裝成單一的 COM + 應用程式，請確定您確實想要在執行未排入佇列的元件時，將佇列的元件啟動。</span><span class="sxs-lookup"><span data-stu-id="a294e-222">While the queued components service can be started in this way, if you package queued and non-queued components into a single COM+ application, be sure that you really want queued components to start if a non-queued component is executed.</span></span> <span data-ttu-id="a294e-223">如果不是這種情況，請將已排入佇列的元件封裝成與其他元件不同的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a294e-223">If this is not the case, package the queued components into a COM+ application that is separate from the other components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a294e-224">相關主題</span><span class="sxs-lookup"><span data-stu-id="a294e-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a294e-225">啟用元件佇列</span><span class="sxs-lookup"><span data-stu-id="a294e-225">Activating Component Queues</span></span>](activating-component-queues.md)
</dt> </dl>

 

 




