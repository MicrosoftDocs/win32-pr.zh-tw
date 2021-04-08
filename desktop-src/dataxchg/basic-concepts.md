---
title: 基本概念
description: 本主題討論有關動態資料交換的重要概念。
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- 'Windows 消費者介面，動態資料交換 (DDE) '
- 'Windows 消費者介面、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) 、用戶端伺服器互動
- DDE (動態資料交換) 、用戶端伺服器互動
- '資料交換、動態資料交換 (DDE) '
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) 、用戶端應用程式
- DDE (動態資料交換) ，用戶端應用程式
- 動態資料交換 (的 DDE) 、伺服器應用程式
- DDE (動態資料交換) 、伺服器應用程式
- 動態資料交換 (DDE) 、回呼函式
- DDE (動態資料交換) ，回呼函式
- 動態資料交換 (DDE) ，交易
- DDE (動態資料交換) ，交易
- 動態資料交換 (的 DDE) ，服務名稱
- DDE (動態資料交換) ，服務名稱
- 動態資料交換 (的 DDE) ，專案名稱
- DDE (動態資料交換) ，專案名稱
- 動態資料交換 (的 DDE) ，主題名稱
- DDE (動態資料交換) ，主題名稱
- 動態資料交換 (DDE) ，系統主題
- DDE (動態資料交換) ，系統主題
- 動態資料交換管理程式庫 (DDEML) 、初始化
- DDEML (動態資料交換管理程式庫) ，初始化
- 動態資料交換管理程式庫 (DDEML) 、回呼函數
- DDEML (動態資料交換管理程式庫) ，回呼函數
- 動態資料交換管理程式庫 (DDEML) 、字串管理
- DDEML (動態資料交換管理程式庫) ，字串管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c564bffbcbb06ddc3a0e0fa4e0a9ed398d3ca55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682512"
---
# <a name="basic-concepts-dde"></a><span data-ttu-id="de248-131"> (DDE) 的基本概念</span><span class="sxs-lookup"><span data-stu-id="de248-131">Basic Concepts (DDE)</span></span>

<span data-ttu-id="de248-132">這些概念是瞭解動態資料交換 (DDE) 以及動態資料交換管理程式庫 (DDEML) 的關鍵。</span><span class="sxs-lookup"><span data-stu-id="de248-132">These concepts are key to understanding Dynamic Data Exchange (DDE) and the Dynamic Data Exchange Management Library (DDEML).</span></span>

-   [<span data-ttu-id="de248-133">用戶端與伺服器互動</span><span class="sxs-lookup"><span data-stu-id="de248-133">Client and Server Interaction</span></span>](#client-and-server-interaction)
-   [<span data-ttu-id="de248-134">交易和 DDE 回呼函數</span><span class="sxs-lookup"><span data-stu-id="de248-134">Transactions and the DDE Callback Function</span></span>](#transactions-and-the-dde-callback-function)
-   [<span data-ttu-id="de248-135">服務名稱、主題名稱和專案名稱</span><span class="sxs-lookup"><span data-stu-id="de248-135">Service Names, Topic Names, and Item Names</span></span>](#service-names-topic-names-and-item-names)
-   [<span data-ttu-id="de248-136">系統主題</span><span class="sxs-lookup"><span data-stu-id="de248-136">System Topic</span></span>](#system-topic)
-   [<span data-ttu-id="de248-137">初始 化</span><span class="sxs-lookup"><span data-stu-id="de248-137">Initialization</span></span>](#initialization)
-   [<span data-ttu-id="de248-138">回呼函數</span><span class="sxs-lookup"><span data-stu-id="de248-138">Callback Function</span></span>](#callback-function)
-   [<span data-ttu-id="de248-139">字串管理</span><span class="sxs-lookup"><span data-stu-id="de248-139">String Management</span></span>](#string-management)
-   [<span data-ttu-id="de248-140">DDEML 和執行緒</span><span class="sxs-lookup"><span data-stu-id="de248-140">DDEML and Threads</span></span>](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a><span data-ttu-id="de248-141">用戶端與伺服器互動</span><span class="sxs-lookup"><span data-stu-id="de248-141">Client and Server Interaction</span></span>

<span data-ttu-id="de248-142">在用戶端應用程式和伺服器應用程式之間一律會發生 DDE。</span><span class="sxs-lookup"><span data-stu-id="de248-142">DDE always occurs between a client application and a server application.</span></span> <span data-ttu-id="de248-143">*DDE 用戶端應用程式* 會建立與伺服器的交談，以將交易傳送到伺服器，藉此起始交換。</span><span class="sxs-lookup"><span data-stu-id="de248-143">The *DDE client application* initiates the exchange by establishing a conversation with the server to send transactions to the server.</span></span> <span data-ttu-id="de248-144">交易是資料或服務的要求。</span><span class="sxs-lookup"><span data-stu-id="de248-144">A transaction is a request for data or services.</span></span> <span data-ttu-id="de248-145">*DDE 伺服器應用程式* 會藉由提供資料或服務給用戶端來回應交易。</span><span class="sxs-lookup"><span data-stu-id="de248-145">The *DDE server application* responds to transactions by providing data or services to the client.</span></span> <span data-ttu-id="de248-146">例如，圖形應用程式可能包含代表公司每季收益的橫條圖，但橫條圖的資料可能包含在試算表應用程式中。</span><span class="sxs-lookup"><span data-stu-id="de248-146">For example, a graphics application might contain a bar graph representing a corporation's quarterly profits, but the data for the bar graph might be contained in a spreadsheet application.</span></span> <span data-ttu-id="de248-147">為了取得最新的收益圖， (用戶端的圖形應用程式) 可以與 (伺服器) 的試算表應用程式建立交談。</span><span class="sxs-lookup"><span data-stu-id="de248-147">To obtain the latest profit figures, the graphics application (the client) could establish a conversation with the spreadsheet application (the server).</span></span> <span data-ttu-id="de248-148">然後，圖形應用程式可以將交易傳送到試算表應用程式，要求最新的收益圖。</span><span class="sxs-lookup"><span data-stu-id="de248-148">The graphics application could then send a transaction to the spreadsheet application, requesting the latest profit figures.</span></span>

<span data-ttu-id="de248-149">伺服器可以同時有許多用戶端，而用戶端可以從多部伺服器要求資料。</span><span class="sxs-lookup"><span data-stu-id="de248-149">A server can have many clients at the same time, and a client can request data from multiple servers.</span></span> <span data-ttu-id="de248-150">應用程式也可以是用戶端和伺服器。</span><span class="sxs-lookup"><span data-stu-id="de248-150">An application can also be both a client and a server.</span></span> <span data-ttu-id="de248-151">用戶端或伺服器隨時都可以終止交談。</span><span class="sxs-lookup"><span data-stu-id="de248-151">Either the client or the server can terminate the conversation at any time.</span></span>

## <a name="transactions-and-the-dde-callback-function"></a><span data-ttu-id="de248-152">交易和 DDE 回呼函數</span><span class="sxs-lookup"><span data-stu-id="de248-152">Transactions and the DDE Callback Function</span></span>

<span data-ttu-id="de248-153">DDEML 會將交易傳送至應用程式的 DDE 回呼函式，以通知應用程式有關的 DDE 活動。</span><span class="sxs-lookup"><span data-stu-id="de248-153">The DDEML notifies an application about DDE activity that affects the application by sending transactions to the application's DDE callback function.</span></span> <span data-ttu-id="de248-154">*DDE 交易* 類似于訊息，它是名為的常數，以及其他包含交易其他資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="de248-154">A *DDE transaction* is similar to a message   it is a named constant accompanied by other parameters that contain additional information about the transaction.</span></span>

<span data-ttu-id="de248-155">DDEML 會將交易傳遞至應用程式定義的 DDE 回呼函式，此函式會執行適合交易類型的動作。</span><span class="sxs-lookup"><span data-stu-id="de248-155">The DDEML passes a transaction to an application-defined DDE callback function that carries out an action appropriate to the type of transaction.</span></span> <span data-ttu-id="de248-156">例如，當用戶端應用程式嘗試建立與伺服器應用程式的對話時，用戶端會呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 函數。</span><span class="sxs-lookup"><span data-stu-id="de248-156">For example, when a client application attempts to establish a conversation with a server application, the client calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span> <span data-ttu-id="de248-157">這個函式會讓 DDEML 將 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易傳送到伺服器的 DDE 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="de248-157">This function causes the DDEML to send an [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="de248-158">回呼函式可以藉由傳回 **TRUE** 給 DDEML 來允許交談，或藉由傳回 **FALSE** 來拒絕交談。</span><span class="sxs-lookup"><span data-stu-id="de248-158">The callback function can allow the conversation by returning **TRUE** to the DDEML, or it can deny the conversation by returning **FALSE**.</span></span> <span data-ttu-id="de248-159">如需交易的詳細討論，請參閱 [交易管理](transaction-management.md)。</span><span class="sxs-lookup"><span data-stu-id="de248-159">For a detailed discussion of transactions, see [Transaction Management](transaction-management.md).</span></span>

## <a name="service-names-topic-names-and-item-names"></a><span data-ttu-id="de248-160">服務名稱、主題名稱和專案名稱</span><span class="sxs-lookup"><span data-stu-id="de248-160">Service Names, Topic Names, and Item Names</span></span>

<span data-ttu-id="de248-161">DDE 伺服器在先前的 DDE 檔中使用三層階層服務名稱 (稱為「應用程式名稱」) 、主題名稱和專案名稱，以唯一識別伺服器在交談期間可以交換的資料單位。</span><span class="sxs-lookup"><span data-stu-id="de248-161">A DDE server uses a three-level hierarchy   service name (called "application name" in previous DDE documentation), topic name, and item name   to uniquely identify a unit of data the server can exchange during a conversation.</span></span>

<span data-ttu-id="de248-162">*服務名稱* 是當用戶端嘗試與伺服器建立交談時，伺服器應用程式所回應的字串。</span><span class="sxs-lookup"><span data-stu-id="de248-162">A *service name* is a string a server application responds to when a client attempts to establish a conversation with the server.</span></span> <span data-ttu-id="de248-163">用戶端必須指定此服務名稱，才能與伺服器建立交談。</span><span class="sxs-lookup"><span data-stu-id="de248-163">A client must specify this service name to establish a conversation with the server.</span></span> <span data-ttu-id="de248-164">雖然伺服器可以回應許多服務名稱，但大部分的伺服器只會回應一個名稱。</span><span class="sxs-lookup"><span data-stu-id="de248-164">Although a server can respond to many service names, most servers respond to only one name.</span></span>

<span data-ttu-id="de248-165">*主題名稱* 是識別邏輯資料內容的字串。</span><span class="sxs-lookup"><span data-stu-id="de248-165">A *topic name* is a string that identifies a logical data context.</span></span> <span data-ttu-id="de248-166">對於在以檔案為基礎的檔上操作的伺服器，主題名稱通常是檔案名;其他伺服器則是其他應用程式特定的字串。</span><span class="sxs-lookup"><span data-stu-id="de248-166">For servers that operate on file-based documents, topic names are typically filenames; for other servers, they are other application-specific strings.</span></span> <span data-ttu-id="de248-167">用戶端必須在嘗試建立與伺服器的對話時，指定主題名稱以及伺服器的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="de248-167">A client must specify a topic name along with a server's service name when it attempts to establish a conversation with a server.</span></span>

<span data-ttu-id="de248-168">*專案名稱* 是一個字串，可識別伺服器在交易期間可以傳遞給用戶端的資料單位。</span><span class="sxs-lookup"><span data-stu-id="de248-168">An *item name* is a string that identifies a unit of data a server can pass to a client during a transaction.</span></span> <span data-ttu-id="de248-169">例如，專案名稱可能會識別整數、字串、數個文欄位落或點陣圖。</span><span class="sxs-lookup"><span data-stu-id="de248-169">For example, an item name might identify an integer, a string, several paragraphs of text, or a bitmap.</span></span>

<span data-ttu-id="de248-170">服務、主題和專案名稱可讓用戶端與伺服器建立交談，以及接收來自伺服器的資料。</span><span class="sxs-lookup"><span data-stu-id="de248-170">The service, topic, and item names enable the client to establish a conversation with a server and to receive data from the server.</span></span>

## <a name="system-topic"></a><span data-ttu-id="de248-171">系統主題</span><span class="sxs-lookup"><span data-stu-id="de248-171">System Topic</span></span>

<span data-ttu-id="de248-172">系統主題提供任何 DDE 用戶端的一般感興趣資訊的內容。</span><span class="sxs-lookup"><span data-stu-id="de248-172">The System topic provides a context for information of general interest to any DDE client.</span></span> <span data-ttu-id="de248-173">建議伺服器應用程式隨時都支援系統主題。</span><span class="sxs-lookup"><span data-stu-id="de248-173">It is recommended that server applications support the System topic at all times.</span></span> <span data-ttu-id="de248-174">系統主題定義于 DDEML 中。H 標頭檔作為 SZDDESYS \_ 主題。</span><span class="sxs-lookup"><span data-stu-id="de248-174">The System topic is defined in the DDEML.H header file as SZDDESYS\_TOPIC.</span></span>

<span data-ttu-id="de248-175">若要判斷有哪些伺服器存在以及它們可以提供的資訊類型，用戶端應用程式可以在啟動時要求系統主題的交談，將裝置名稱設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="de248-175">To determine which servers are present and the kinds of information they can provide, a client application can request a conversation on the System topic upon starting, setting the device name to **NULL**.</span></span> <span data-ttu-id="de248-176">這類萬用字元交談在系統效能方面相當昂貴，因此應該保持最小值。</span><span class="sxs-lookup"><span data-stu-id="de248-176">Such wildcard conversations are costly in terms of system performance, so they should be kept to a minimum.</span></span> <span data-ttu-id="de248-177">如需有關起始 DDE 交談的詳細資訊，請參閱 [對話管理](conversation-management.md)。</span><span class="sxs-lookup"><span data-stu-id="de248-177">For more information about initiating DDE conversations, see [Conversation Management](conversation-management.md).</span></span>

<span data-ttu-id="de248-178">伺服器必須支援系統主題內的下列專案名稱，以及對用戶端有用的任何其他專案名稱。</span><span class="sxs-lookup"><span data-stu-id="de248-178">A server must support the following item names within the System topic and any other item names that are useful to a client.</span></span>



| <span data-ttu-id="de248-179">項目</span><span class="sxs-lookup"><span data-stu-id="de248-179">Item</span></span>                     | <span data-ttu-id="de248-180">描述</span><span class="sxs-lookup"><span data-stu-id="de248-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de248-181">SZDDE \_ 專案 \_ ITEMLIST</span><span class="sxs-lookup"><span data-stu-id="de248-181">SZDDE\_ITEM\_ITEMLIST</span></span>    | <span data-ttu-id="de248-182">非系統主題下支援的專案清單。</span><span class="sxs-lookup"><span data-stu-id="de248-182">A list of the items supported under a non-System topic.</span></span> <span data-ttu-id="de248-183"> (這份清單會隨著時間和主題的不同而有所不同。 ) </span><span class="sxs-lookup"><span data-stu-id="de248-183">(This list can vary from moment to moment and from topic to topic.)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="de248-184">SZDDESYS \_ 專案 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="de248-184">SZDDESYS\_ITEM\_FORMATS</span></span>  | <span data-ttu-id="de248-185">以定位字元分隔的字串清單，表示服務應用程式可能支援的所有剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="de248-185">A tab-delimited list of strings representing all clipboard formats potentially supported by the service application.</span></span> <span data-ttu-id="de248-186">代表預先定義剪貼簿格式的字串相當於 \_ 已移除 "CF" 前置詞的 C光圈值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de248-186">Strings that represent predefined clipboard formats are equivalent to the CF\_ values with the "CF\_" prefix removed.</span></span> <span data-ttu-id="de248-187">例如，CF \_ 文字格式是以字串 "text" 表示。</span><span class="sxs-lookup"><span data-stu-id="de248-187">For example, the CF\_TEXT format is represented by the string "TEXT".</span></span> <span data-ttu-id="de248-188">這些字串必須是大寫，才能進一步將其識別為預先定義的格式。</span><span class="sxs-lookup"><span data-stu-id="de248-188">These strings must be uppercase to further identify them as predefined formats.</span></span> <span data-ttu-id="de248-189">格式清單必須以最豐富的內容順序出現在內容中，而不是最豐富的內容。</span><span class="sxs-lookup"><span data-stu-id="de248-189">The list of formats must appear in the order of most rich in content to least rich in content.</span></span> <span data-ttu-id="de248-190">如需剪貼簿格式和轉譯資料的詳細資訊，請參閱 [剪貼](clipboard.md)簿。</span><span class="sxs-lookup"><span data-stu-id="de248-190">For more information about clipboard formats and rendering data, see [Clipboard](clipboard.md).</span></span><br/> |
| <span data-ttu-id="de248-191">SZDDESYS \_ 專案 \_ 說明</span><span class="sxs-lookup"><span data-stu-id="de248-191">SZDDESYS\_ITEM\_HELP</span></span>     | <span data-ttu-id="de248-192">一般感興趣的使用者可讀取資訊。</span><span class="sxs-lookup"><span data-stu-id="de248-192">User-readable information of general interest.</span></span> <span data-ttu-id="de248-193">此專案至少必須包含有關如何使用伺服器應用程式之 DDE 功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="de248-193">This item must contain, at a minimum, information on how to use the server application's DDE features.</span></span> <span data-ttu-id="de248-194">這項資訊可包括（但不限於）如何指定主題中的專案、伺服器可執行檔執行字串、允許的內容，以及如何在其他系統主題專案中尋找說明。</span><span class="sxs-lookup"><span data-stu-id="de248-194">This information can include, but is not limited to, how to specify items within topics, what execute strings the server can perform, what poke transactions are allowed, and how to find help on other System topic items.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="de248-195">SZDDESYS \_ 專案 \_ RTNMSG</span><span class="sxs-lookup"><span data-stu-id="de248-195">SZDDESYS\_ITEM\_RTNMSG</span></span>   | <span data-ttu-id="de248-196">最近使用之 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息的支援詳細資料。</span><span class="sxs-lookup"><span data-stu-id="de248-196">Supporting detail for the most recently used [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="de248-197">當需要超過8個位的應用程式特定傳回資料時，此專案很有用。</span><span class="sxs-lookup"><span data-stu-id="de248-197">This item is useful when more than 8 bits of application-specific return data are required.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="de248-198">SZDDESYS \_ 專案 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="de248-198">SZDDESYS\_ITEM\_STATUS</span></span>   | <span data-ttu-id="de248-199">指出伺服器目前狀態的指示。</span><span class="sxs-lookup"><span data-stu-id="de248-199">An indication of the current status of the server.</span></span> <span data-ttu-id="de248-200">一般來說，這個專案僅支援 CF \_ 文字格式，並且包含就緒或忙碌的字串。</span><span class="sxs-lookup"><span data-stu-id="de248-200">Typically, this item supports only the CF\_TEXT format and contains the Ready or Busy string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="de248-201">SZDDESYS \_ 專案 \_ SYSITEMS</span><span class="sxs-lookup"><span data-stu-id="de248-201">SZDDESYS\_ITEM\_SYSITEMS</span></span> | <span data-ttu-id="de248-202">此伺服器在系統主題下支援的專案清單。</span><span class="sxs-lookup"><span data-stu-id="de248-202">A list of the items supported under the System topic by this server.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="de248-203">SZDDESYS \_ 專案 \_ 主題</span><span class="sxs-lookup"><span data-stu-id="de248-203">SZDDESYS\_ITEM\_TOPICS</span></span>   | <span data-ttu-id="de248-204">伺服器在目前時間所支援的主題清單。</span><span class="sxs-lookup"><span data-stu-id="de248-204">A list of the topics supported by the server at the current time.</span></span> <span data-ttu-id="de248-205"> (這份清單可能會有不同的時間。 ) </span><span class="sxs-lookup"><span data-stu-id="de248-205">(This list can vary from moment to moment.)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="de248-206">這些專案名稱是在 DDEML 中定義的值。H 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="de248-206">These item names are values defined in the DDEML.H header file.</span></span> <span data-ttu-id="de248-207">若要取得這些字串的字串控制碼，應用程式必須使用 DDEML 字串管理函式，就像在 DDEML 應用程式中的任何其他字串一樣。</span><span class="sxs-lookup"><span data-stu-id="de248-207">To obtain string handles to these strings, an application must use the DDEML string-management functions, just as it would for any other string in a DDEML application.</span></span> <span data-ttu-id="de248-208">如需管理字串的詳細資訊，請參閱 [字串管理](#string-management)。</span><span class="sxs-lookup"><span data-stu-id="de248-208">For more information about managing strings, see [String Management](#string-management).</span></span>

## <a name="initialization"></a><span data-ttu-id="de248-209">初始化</span><span class="sxs-lookup"><span data-stu-id="de248-209">Initialization</span></span>

<span data-ttu-id="de248-210">在呼叫任何其他 DDEML 函式之前，應用程式必須呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函數。</span><span class="sxs-lookup"><span data-stu-id="de248-210">Before calling any other DDEML function, an application must call the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="de248-211">**DdeInitialize** 會取得應用程式的實例識別碼、使用 dde 來註冊應用程式的 dde 回呼函式，並指定回呼函數的交易篩選旗標。</span><span class="sxs-lookup"><span data-stu-id="de248-211">**DdeInitialize** obtains an instance identifier for the application, registers the application's DDE callback function with the DDE, and specifies the transaction filter flags for the callback function.</span></span>

<span data-ttu-id="de248-212">應用程式或 DLL 的每個實例都必須將其實例識別碼作為 *idInst* 參數傳遞給任何其他需要它的 DDEML 函數。</span><span class="sxs-lookup"><span data-stu-id="de248-212">Each instance of an application or a DLL must pass its instance identifier as the *idInst* parameter to any other DDEML function that requires it.</span></span> <span data-ttu-id="de248-213">多個 DDEML 實例的目的是要支援在應用程式使用 DDEML 時，必須同時使用該的 Dll。</span><span class="sxs-lookup"><span data-stu-id="de248-213">The purpose of multiple DDEML instances is to support DLLs that must use the DDEML at the same time an application is using it.</span></span> <span data-ttu-id="de248-214">應用程式不能使用一個以上的 DDEML 實例。</span><span class="sxs-lookup"><span data-stu-id="de248-214">An application must not use more than one instance of the DDEML.</span></span>

<span data-ttu-id="de248-215">*交易篩選* 會防止 DDEML 將不需要的交易傳遞到應用程式的 DDE 回呼函式，以優化系統效能。</span><span class="sxs-lookup"><span data-stu-id="de248-215">*Transaction filters* optimize system performance by preventing the DDEML from passing unwanted transactions to the application's DDE callback function.</span></span> <span data-ttu-id="de248-216">應用程式會在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* 參數中設定交易篩選。</span><span class="sxs-lookup"><span data-stu-id="de248-216">An application sets the transaction filters in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* parameter.</span></span> <span data-ttu-id="de248-217">應用程式必須為每一種交易類型指定交易篩選旗標，但它不會在其回呼函數中處理。</span><span class="sxs-lookup"><span data-stu-id="de248-217">An application must specify a transaction filter flag for each type of transaction that it does not process in its callback function.</span></span> <span data-ttu-id="de248-218">應用程式可以使用 **DdeInitialize** 的後續呼叫來變更其交易篩選。</span><span class="sxs-lookup"><span data-stu-id="de248-218">An application can change its transaction filters with a subsequent call to **DdeInitialize**.</span></span> <span data-ttu-id="de248-219">如需交易的詳細資訊，請參閱 [交易管理](transaction-management.md)。</span><span class="sxs-lookup"><span data-stu-id="de248-219">For more information about transactions, see [Transaction Management](transaction-management.md).</span></span>

<span data-ttu-id="de248-220">下列範例示範如何初始化應用程式以使用 DDEML。</span><span class="sxs-lookup"><span data-stu-id="de248-220">The following example shows how to initialize an application to use the DDEML.</span></span>


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



<span data-ttu-id="de248-221">當應用程式不再使用 DDEML 時，必須呼叫 [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) 函數。</span><span class="sxs-lookup"><span data-stu-id="de248-221">An application must call the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function when it is no longer going to use the DDEML.</span></span> <span data-ttu-id="de248-222">此函式會終止應用程式目前開啟的所有交談，並釋出系統組態給應用程式的 DDEML 資源。</span><span class="sxs-lookup"><span data-stu-id="de248-222">This function terminates any conversations currently open for the application and frees the DDEML resources the system allocated for the application.</span></span>

## <a name="callback-function"></a><span data-ttu-id="de248-223">回呼函式</span><span class="sxs-lookup"><span data-stu-id="de248-223">Callback Function</span></span>

<span data-ttu-id="de248-224">使用 DDEML 的應用程式必須提供回呼函式，以處理影響應用程式的 DDE 事件。</span><span class="sxs-lookup"><span data-stu-id="de248-224">An application that uses the DDEML must provide a callback function that processes the DDE events affecting the application.</span></span> <span data-ttu-id="de248-225">DDEML 會將交易傳送至應用程式的 DDE 回呼函式，以通知應用這類事件。</span><span class="sxs-lookup"><span data-stu-id="de248-225">The DDEML notifies an application of such events by sending transactions to the application's DDE callback function.</span></span> <span data-ttu-id="de248-226">回呼函數接收的交易取決於 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 中指定的應用程式，以及應用程式是用戶端、伺服器或兩者。</span><span class="sxs-lookup"><span data-stu-id="de248-226">The transactions a callback function receives depend on which callback filter flags the application specified in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) and whether the application is a client, a server, or both.</span></span> <span data-ttu-id="de248-227">如需詳細資訊，請參閱 [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback)。</span><span class="sxs-lookup"><span data-stu-id="de248-227">For more information, please see [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).</span></span>

<span data-ttu-id="de248-228">下列範例顯示一般用戶端應用程式的回呼函式的一般結構。</span><span class="sxs-lookup"><span data-stu-id="de248-228">The following example shows the general structure of a callback function for a typical client application.</span></span>


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



<span data-ttu-id="de248-229">*UType* 參數會指定 DDEML 傳送給回呼函數的交易類型。</span><span class="sxs-lookup"><span data-stu-id="de248-229">The *uType* parameter specifies the transaction type sent to the callback function by the DDEML.</span></span> <span data-ttu-id="de248-230">其餘參數的值取決於交易類型。</span><span class="sxs-lookup"><span data-stu-id="de248-230">The values of the remaining parameters depend on the transaction type.</span></span> <span data-ttu-id="de248-231">下列主題將說明產生它們的交易類型和事件。</span><span class="sxs-lookup"><span data-stu-id="de248-231">The transaction types and the events that generate them are described in the following topics.</span></span> <span data-ttu-id="de248-232">如需每種交易類型的詳細資訊，請參閱 [交易管理](transaction-management.md)。</span><span class="sxs-lookup"><span data-stu-id="de248-232">For detailed information about each transaction type, see [Transaction Management](transaction-management.md).</span></span>

## <a name="string-management"></a><span data-ttu-id="de248-233">字串管理</span><span class="sxs-lookup"><span data-stu-id="de248-233">String Management</span></span>

<span data-ttu-id="de248-234">為了執行 DDE 工作，許多 DDEML 函式都需要存取字串。</span><span class="sxs-lookup"><span data-stu-id="de248-234">To carry out a DDE task, many DDEML functions require access to strings.</span></span> <span data-ttu-id="de248-235">例如，當用戶端呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 函數來要求與伺服器的對話時，用戶端必須指定服務名稱和主題名稱。</span><span class="sxs-lookup"><span data-stu-id="de248-235">For example, a client must specify a service name and a topic name when it calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function to request a conversation with a server.</span></span> <span data-ttu-id="de248-236">應用程式會藉由傳遞字串控制碼 (HSZ) （而不是 DDEML 函式中的指標）來指定字串。</span><span class="sxs-lookup"><span data-stu-id="de248-236">An application specifies a string by passing a string handle (HSZ) rather than a pointer in a DDEML function.</span></span> <span data-ttu-id="de248-237">*字串控制碼* 是系統指派的 **DWORD** 值，可識別字串。</span><span class="sxs-lookup"><span data-stu-id="de248-237">A *string handle* is a **DWORD** value, assigned by the system, that identifies a string.</span></span>

<span data-ttu-id="de248-238">應用程式可以藉由呼叫 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) 函數，取得特定字串的字串控制碼。</span><span class="sxs-lookup"><span data-stu-id="de248-238">An application can obtain a string handle to a particular string by calling the [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) function.</span></span> <span data-ttu-id="de248-239">此函式會向系統註冊字串，並將字串控制碼傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="de248-239">This function registers the string with the system and returns a string handle to the application.</span></span> <span data-ttu-id="de248-240">應用程式可以將控制碼傳遞給必須存取字串的 DDEML 函數。</span><span class="sxs-lookup"><span data-stu-id="de248-240">The application can pass the handle to DDEML functions that must access the string.</span></span> <span data-ttu-id="de248-241">下列範例會取得系統主題字串和服務名稱字串的字串控制碼。</span><span class="sxs-lookup"><span data-stu-id="de248-241">The following example obtains string handles to the System topic string and the service name string.</span></span>


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



<span data-ttu-id="de248-242">上述範例中的 *idInst* 參數會指定 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函數所取得的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="de248-242">The *idInst* parameter in the preceding example specifies the instance identifier obtained by the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="de248-243">應用程式的 DDE 回呼函數會在大部分的 DDE 交易期間收到一或多個字串控制碼。</span><span class="sxs-lookup"><span data-stu-id="de248-243">An application's DDE callback function receives one or more string handles during most DDE transactions.</span></span> <span data-ttu-id="de248-244">例如，伺服器會在 [**XTYP \_ 要求**](xtyp-request.md) 交易期間收到兩個字串控制碼：一個會識別指定主題名稱的字串，另一個則會識別指定專案名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="de248-244">For example, a server receives two string handles during the [**XTYP\_REQUEST**](xtyp-request.md) transaction: one identifies a string specifying a topic name, and the other identifies a string specifying an item name.</span></span> <span data-ttu-id="de248-245">應用程式可以藉由呼叫 [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) 函式來取得對應于字串控制碼的字串長度，並將字串複製到應用程式定義的緩衝區，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="de248-245">An application can obtain the length of the string that corresponds to a string handle and copy the string to an application-defined buffer by calling the [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) function, as shown in the following example.</span></span>


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



<span data-ttu-id="de248-246">實例特定的字串控制碼無法從字串控制碼對應到字串，也不能對應回字串控制碼。</span><span class="sxs-lookup"><span data-stu-id="de248-246">An instance-specific string handle cannot be mapped from string handle to string and back to string handle.</span></span> <span data-ttu-id="de248-247">例如，雖然 [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) 會從字串控制碼建立字串，然後 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) 從該字串建立字串控制碼，但兩個控制碼並不相同，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="de248-247">For instance, although [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) creates a string from a string handle and then [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) creates a string handle from that string, the two handles are not the same, as shown in the following example.</span></span>


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



<span data-ttu-id="de248-248">若要比較兩個字串控制碼的值，請使用 [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) 函數。</span><span class="sxs-lookup"><span data-stu-id="de248-248">To compare the values of two string handles, use the [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) function.</span></span>

<span data-ttu-id="de248-249">當回呼函式傳回時，傳遞給應用程式之 DDE 回呼函數的字串控制碼會變成無效。</span><span class="sxs-lookup"><span data-stu-id="de248-249">A string handle passed to an application's DDE callback function becomes invalid when the callback function returns.</span></span> <span data-ttu-id="de248-250">應用程式可以使用 [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) 函式來儲存回呼函數傳回後使用的字串控制碼。</span><span class="sxs-lookup"><span data-stu-id="de248-250">An application can save a string handle for use after the callback function returns by using the [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) function.</span></span>

<span data-ttu-id="de248-251">當應用程式呼叫 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea)時，系統會將指定的字串輸入字串資料表中，並產生用來存取字串的控制碼。</span><span class="sxs-lookup"><span data-stu-id="de248-251">When an application calls [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), the system enters the specified string into a string table and generates a handle that it uses to access the string.</span></span> <span data-ttu-id="de248-252">系統也會維護字串資料表中每個字串的使用計數。</span><span class="sxs-lookup"><span data-stu-id="de248-252">The system also maintains a usage count for each string in the string table.</span></span>

<span data-ttu-id="de248-253">當應用程式呼叫 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) 並指定已經存在於資料表中的字串時，系統會遞增使用量計數，而不是加入另一次出現的字串。</span><span class="sxs-lookup"><span data-stu-id="de248-253">When an application calls [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) and specifies a string that already exists in the table, the system increments the usage count rather than adding another occurrence of the string.</span></span> <span data-ttu-id="de248-254"> (應用程式也可以使用 [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle)來遞增使用量計數。 ) 當應用程式呼叫 [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) 函式時，系統會遞減使用計數。</span><span class="sxs-lookup"><span data-stu-id="de248-254">(An application can also increment the usage count by using [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle).) When an application calls the [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) function, the system decrements the usage count.</span></span>

<span data-ttu-id="de248-255">當字串的使用計數等於零時，就會從資料表中移除字串。</span><span class="sxs-lookup"><span data-stu-id="de248-255">A string is removed from the table when its usage count equals zero.</span></span> <span data-ttu-id="de248-256">由於有一個以上的應用程式可以取得特定字串的控制碼，因此應用程式不能將字串控制碼釋出超過其建立或保留控制碼的次數。</span><span class="sxs-lookup"><span data-stu-id="de248-256">Because more than one application can obtain the handle to a particular string, an application must not free a string handle more times than it has created or retained the handle.</span></span> <span data-ttu-id="de248-257">否則，應用程式可能會從資料表中移除字串，而拒絕其他應用程式存取字串。</span><span class="sxs-lookup"><span data-stu-id="de248-257">Otherwise, the application can cause the string to be removed from the table, denying other applications access to the string.</span></span>

<span data-ttu-id="de248-258">DDEML 字串管理函式是以 atom 管理員為基礎，且受限於與原子相同的大小限制。</span><span class="sxs-lookup"><span data-stu-id="de248-258">The DDEML string-management functions are based on the atom manager and are subject to the same size restrictions as are atoms.</span></span>

## <a name="ddeml-and-threads"></a><span data-ttu-id="de248-259">DDEML 和執行緒</span><span class="sxs-lookup"><span data-stu-id="de248-259">DDEML and Threads</span></span>

<span data-ttu-id="de248-260">[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式會向 DDEML 註冊應用程式，並建立 DDEML 實例。</span><span class="sxs-lookup"><span data-stu-id="de248-260">The [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function registers an application with the DDEML, creating a DDEML instance.</span></span> <span data-ttu-id="de248-261">DDEML 實例是以執行緒為基礎，與呼叫 **DdeInitialize** 的執行緒相關聯。</span><span class="sxs-lookup"><span data-stu-id="de248-261">A DDEML instance is thread-based, associated with the thread that called **DdeInitialize**.</span></span>

<span data-ttu-id="de248-262">屬於 DDEML 實例之物件的所有 DDEML 函式呼叫，都必須從呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 的相同執行緒建立實例。</span><span class="sxs-lookup"><span data-stu-id="de248-262">All DDEML function calls for objects belonging to a DDEML instance must be made from the same thread that called [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) to create the instance.</span></span> <span data-ttu-id="de248-263">如果您從不同的執行緒呼叫 DDEML 函式，此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="de248-263">If you call a DDEML function from a different thread, the function will fail.</span></span> <span data-ttu-id="de248-264">您無法從配置交談以外的執行緒存取 DDEML 交談。</span><span class="sxs-lookup"><span data-stu-id="de248-264">You cannot access a DDEML conversation from a thread other than the one that allocated the conversation.</span></span>

 

