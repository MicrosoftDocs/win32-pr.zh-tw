---
title: 'Windows 事件記錄檔錯誤常數 (Winerror.h .h) '
description: 以下是 Windows 事件記錄檔所定義的錯誤碼。
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5443d98c53d6abedbe3a0027e8e2e524ae9df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965529"
---
# <a name="windows-event-log-error-constants"></a><span data-ttu-id="3b2e3-103">Windows 事件記錄檔錯誤常數</span><span class="sxs-lookup"><span data-stu-id="3b2e3-103">Windows Event Log Error Constants</span></span>

<span data-ttu-id="3b2e3-104">以下是 Windows 事件記錄檔所定義的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-104">The following are the error codes that Windows Event Log defines.</span></span>

<dl> <dt>

<span data-ttu-id="3b2e3-105"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-105"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-106">15000</span><span class="sxs-lookup"><span data-stu-id="3b2e3-106">15000</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-107">指定的通道路徑無效。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-107">The specified channel path is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-108"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**錯誤 \_ .EVT \_ 不正確 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-108"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-109">15001</span><span class="sxs-lookup"><span data-stu-id="3b2e3-109">15001</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-110">指定的查詢無效。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-110">The specified query is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-111"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**\_ \_ \_ \_ 找不到簽發者中繼資料 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-111"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-112">15002</span><span class="sxs-lookup"><span data-stu-id="3b2e3-112">15002</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-113">在資源中找不到提供者中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-113">The provider metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-114"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件範本**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-114"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-115">15003</span><span class="sxs-lookup"><span data-stu-id="3b2e3-115">15003</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-116">資源中找不到事件定義的範本。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-116">The template for an event definition cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-117"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-117"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-118">15004</span><span class="sxs-lookup"><span data-stu-id="3b2e3-118">15004</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-119">指定的提供者名稱無效。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-119">The specified provider name is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-120"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**錯誤 \_ .EVT \_ 不正確 \_ 事件 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-120"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-121">15005</span><span class="sxs-lookup"><span data-stu-id="3b2e3-121">15005</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-122">提供者所引發的事件資料與提供者資訊清單中的事件範本定義不相容。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-122">The event data raised by the provider is not compatible with the event template definition in the provider's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-123"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 頻道**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-123"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-124">15007</span><span class="sxs-lookup"><span data-stu-id="3b2e3-124">15007</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-125">找不到指定的通道。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-125">The specified channel cannot be found.</span></span> <span data-ttu-id="3b2e3-126">檢查通道設定。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-126">Check the channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-127"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**錯誤 \_ .EVT \_ 格式不正確的 \_ XML \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-127"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-128">15008</span><span class="sxs-lookup"><span data-stu-id="3b2e3-128">15008</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-129">指定的 XML 文字格式不正確。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-129">The specified XML text was not well-formed.</span></span> <span data-ttu-id="3b2e3-130">如需詳細資訊，請呼叫 [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) 函數。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-130">For more information, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-131"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_ \_ \_ 對 \_ 直接 \_ 通道的錯誤 .EVT 訂用帳戶**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-131"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-132">15009</span><span class="sxs-lookup"><span data-stu-id="3b2e3-132">15009</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-133">您無法訂閱分析或 Debug 通道;分析或 Debug 通道的事件會直接移至記錄檔，而且無法訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-133">You cannot subscribe to an Analytic or Debug channel; the events for an Analytic or Debug channel go directly to a log file and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-134"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**錯誤 \_ .EVT \_ 設定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-134"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-135">15010</span><span class="sxs-lookup"><span data-stu-id="3b2e3-135">15010</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-136">發生設定錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-136">A configuration error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-137"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 過時**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-137"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-138">15011</span><span class="sxs-lookup"><span data-stu-id="3b2e3-138">15011</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-139">查詢結果無效。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-139">The query result is not valid.</span></span> <span data-ttu-id="3b2e3-140">這可能是因為在建立查詢結果之後清除或變換記錄所致。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-140">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="3b2e3-141">釋放查詢結果物件並重新發出查詢。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-141">Release the query result object and reissue the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-142"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 不正確 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-142"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-143">15012</span><span class="sxs-lookup"><span data-stu-id="3b2e3-143">15012</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-144">查詢結果的游標未指向有效的位置。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-144">The cursor for the query result is not pointing to a valid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-145"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**錯誤 \_ .EVT \_ 非 \_ 驗證 \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-145"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-146">15013</span><span class="sxs-lookup"><span data-stu-id="3b2e3-146">15013</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-147">註冊的 MSXML 剖析器不支援驗證。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-147">The registered MSXML parser does not support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-148"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**錯誤 \_ .EVT \_ 篩選 \_ ALREADYSCOPED**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-148"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-149">15014</span><span class="sxs-lookup"><span data-stu-id="3b2e3-149">15014</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-150">只有當運算式評估為節點集，且不屬於範圍作業的一些其他變更時，運算式才可以接著變更範圍作業。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-150">An expression can be followed by a change of scope operation only if the expression evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-151"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**錯誤 \_ .EVT \_ 篩選 \_ NOTELTSET**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-151"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-152">15015</span><span class="sxs-lookup"><span data-stu-id="3b2e3-152">15015</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-153">無法從不代表元素集的詞彙執行步驟運算。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-153">Cannot perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-154"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVARG**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-154"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-155">15016</span><span class="sxs-lookup"><span data-stu-id="3b2e3-155">15016</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-156">二元運算子左邊的引數必須是屬性、節點或變數，且右邊的引數必須是常數。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-156">The arguments on the left side of a binary operator must be either attributes, nodes, or variables, and the arguments on the right side must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-157"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTEST**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-157"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-158">15017</span><span class="sxs-lookup"><span data-stu-id="3b2e3-158">15017</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-159">步驟作業必須牽涉到節點測試，或者，若為述詞，則可評估上一個節點集合所識別之節點集內每個節點的代數運算式。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-159">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-160"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTYPE .。。**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-160"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-161">15018</span><span class="sxs-lookup"><span data-stu-id="3b2e3-161">15018</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-162">不支援此資料類型。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-162">This data type not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-163"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**錯誤 \_ .EVT \_ 篩選 \_ PARSEERR**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-163"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-164">15019</span><span class="sxs-lookup"><span data-stu-id="3b2e3-164">15019</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-165">在指定的位置發生語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-165">A syntax error occurred at the specified position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-166"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNSUPPORTEDOP**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-166"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-167">15020</span><span class="sxs-lookup"><span data-stu-id="3b2e3-167">15020</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-168">此篩選準則的執行不支援這個運算子。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-168">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-169"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNEXPECTEDTOKEN**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-169"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-170">15021</span><span class="sxs-lookup"><span data-stu-id="3b2e3-170">15021</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-171">發現未預期的權杖。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-171">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-172"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**錯誤 \_ .EVT \_ \_ 啟用的 \_ \_ \_ 直接 \_ 通道上有不正確操作**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-172"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-173">15022</span><span class="sxs-lookup"><span data-stu-id="3b2e3-173">15022</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-174">無法在已啟用的分析或偵測通道上執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-174">The requested operation cannot be performed over an enabled Analytic or Debug channel.</span></span> <span data-ttu-id="3b2e3-175">您必須先停用通道，才能執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-175">You must disable the channel before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-176"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 屬性 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-176"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-177">15023</span><span class="sxs-lookup"><span data-stu-id="3b2e3-177">15023</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-178">通道屬性包含不正確值。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-178">The channel property contains a value that is not valid.</span></span> <span data-ttu-id="3b2e3-179">值的類型可能無效、值可能超出範圍，或無法更新此類型的通道或不支援的值。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-179">The value's type may not be valid, the value may be out of range, or the value cannot be updated or is not supported for this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-180"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 屬性 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-180"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-181">15024</span><span class="sxs-lookup"><span data-stu-id="3b2e3-181">15024</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-182">Provider 屬性包含不正確值。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-182">The provider property contains a value that is not valid.</span></span> <span data-ttu-id="3b2e3-183">值的類型可能無效、值可能超出範圍，或無法更新此值或不支援此類型的提供者。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-183">The value's type may not be valid, the value may be out of range, or the value cannot be updated or is not supported for this type of provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-184"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**錯誤 \_ .EVT \_ 通道 \_ 無法 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-184"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-185">15025</span><span class="sxs-lookup"><span data-stu-id="3b2e3-185">15025</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-186">通道無法啟動。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-186">The channel failed to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-187"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**錯誤 \_ .EVT \_ 篩選 \_ 太 \_ 複雜**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-187"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-188">15026</span><span class="sxs-lookup"><span data-stu-id="3b2e3-188">15026</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-189">XPath 運算式超過支援的複雜度。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-189">The XPath expression exceeded supported complexity.</span></span> <span data-ttu-id="3b2e3-190">簡化運算式或將其分割成兩個或多個簡單運算式。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-190">Simplify the expression or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-191"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 訊息**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-191"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-192">15027</span><span class="sxs-lookup"><span data-stu-id="3b2e3-192">15027</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-193">訊息資源存在，但在字串或訊息資料表中找不到訊息。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-193">The message resource is present, but the message is not found in the string or message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-194"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息識別碼**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-194"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-195">15028</span><span class="sxs-lookup"><span data-stu-id="3b2e3-195">15028</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-196">找不到訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-196">The message identifier cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-197"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 值 \_ 插入**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-197"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-198">15029</span><span class="sxs-lookup"><span data-stu-id="3b2e3-198">15029</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-199">找不到插入索引的替代字串。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-199">The substitution string for the insert index cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-200"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 參數 \_ 插入**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-200"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-201">15030</span><span class="sxs-lookup"><span data-stu-id="3b2e3-201">15030</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-202">找不到參數參考 (% 1) 的描述字串。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-202">The description string for parameter reference (%1) cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-203"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**已 \_ 達到錯誤的 .EVT \_ 最大 \_ 插入 \_ 數**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-203"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-204">15031</span><span class="sxs-lookup"><span data-stu-id="3b2e3-204">15031</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-205">已達到最大取代數目。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-205">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-206"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件定義**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-206"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-207">15032</span><span class="sxs-lookup"><span data-stu-id="3b2e3-207">15032</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-208">找不到事件識別碼的事件定義。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-208">The event definition cannot be found for the event identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-209"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息地區設定**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-209"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-210">15033</span><span class="sxs-lookup"><span data-stu-id="3b2e3-210">15033</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-211">所需訊息的地區設定特定資源不存在。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-211">The locale-specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-212"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**錯誤的 \_ .EVT \_ 版本 \_ 太 \_ 舊**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-212"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-213">15034</span><span class="sxs-lookup"><span data-stu-id="3b2e3-213">15034</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-214">資源太舊而無法相容。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-214">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-215"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**錯誤 \_ .EVT \_ 版本 \_ 太 \_ 新**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-215"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-216">15035</span><span class="sxs-lookup"><span data-stu-id="3b2e3-216">15035</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-217">資源太新，無法相容。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-217">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-218"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**錯誤 \_ .EVT \_ 無法 \_ 開啟 \_ \_ 查詢通道 \_**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-218"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-219">15036</span><span class="sxs-lookup"><span data-stu-id="3b2e3-219">15036</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-220">無法開啟位於指定之查詢索引的通道。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-220">The channel at the specified index of the query cannot be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-221"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**錯誤的 \_ .EVT \_ 發行者 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-221"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-222">15037</span><span class="sxs-lookup"><span data-stu-id="3b2e3-222">15037</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-223">提供者已停用，且其資源無法使用。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-223">The provider has been disabled and its resources are not available.</span></span> <span data-ttu-id="3b2e3-224">卸載或升級提供者時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-224">This can occur when the provider is uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3b2e3-225"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**錯誤 \_ .EVT \_ 篩選 \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="3b2e3-225"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b2e3-226">15038</span><span class="sxs-lookup"><span data-stu-id="3b2e3-226">15038</span></span>
</dt> <dt>



<span data-ttu-id="3b2e3-227">嘗試建立的數數值型別超出其有效範圍。</span><span class="sxs-lookup"><span data-stu-id="3b2e3-227">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b2e3-228">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b2e3-228">Requirements</span></span>



| <span data-ttu-id="3b2e3-229">需求</span><span class="sxs-lookup"><span data-stu-id="3b2e3-229">Requirement</span></span> | <span data-ttu-id="3b2e3-230">值</span><span class="sxs-lookup"><span data-stu-id="3b2e3-230">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2e3-231">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b2e3-231">Minimum supported client</span></span><br/> | <span data-ttu-id="3b2e3-232">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b2e3-232">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b2e3-233">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b2e3-233">Minimum supported server</span></span><br/> | <span data-ttu-id="3b2e3-234">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b2e3-234">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b2e3-235">標頭</span><span class="sxs-lookup"><span data-stu-id="3b2e3-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b2e3-236"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b2e3-236"><dt>WinError.h</dt></span></span> </dl> |



 

 





