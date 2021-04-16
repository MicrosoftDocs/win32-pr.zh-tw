---
description: 說明憑證服務如何處理憑證要求。
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: 處理憑證要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551093"
---
# <a name="processing-certificate-requests"></a><span data-ttu-id="b821e-103">處理憑證要求</span><span class="sxs-lookup"><span data-stu-id="b821e-103">Processing Certificate Requests</span></span>

<span data-ttu-id="b821e-104">憑證服務會在處理 [*憑證要求*](../secgloss/c-gly.md)時執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b821e-104">Certificate Services performs the following steps when processing a [*certificate request*](../secgloss/c-gly.md):</span></span>

1.  <span data-ttu-id="b821e-105">要求接收。</span><span class="sxs-lookup"><span data-stu-id="b821e-105">Request reception.</span></span>

    <span data-ttu-id="b821e-106">用戶端會將 [*憑證要求*](../secgloss/c-gly.md) 傳送到中繼應用程式，並將其格式化為 PKCS \# 10 格式要求，並將它提交至伺服器引擎。</span><span class="sxs-lookup"><span data-stu-id="b821e-106">The [*certificate request*](../secgloss/c-gly.md) is sent by the client to an intermediary application, which formats it into a PKCS \#10 format request and submits it to the server engine.</span></span>

2.  <span data-ttu-id="b821e-107">要求核准。</span><span class="sxs-lookup"><span data-stu-id="b821e-107">Request approval.</span></span>

    <span data-ttu-id="b821e-108">伺服器引擎會呼叫 [原則模組](policy-modules.md)，此模組會查詢要求屬性、決定要求是否已獲授權，並設定選用的憑證屬性。</span><span class="sxs-lookup"><span data-stu-id="b821e-108">The server engine calls the [Policy Module](policy-modules.md), which queries request properties, decides whether the request is authorized or not, and sets optional certificate properties.</span></span>

3.  <span data-ttu-id="b821e-109">憑證的形式。</span><span class="sxs-lookup"><span data-stu-id="b821e-109">Certificate formation.</span></span>

    <span data-ttu-id="b821e-110">如果要求已核准，則伺服器引擎會接受要求和原則模組所要求的任何屬性，並建立完整的憑證。</span><span class="sxs-lookup"><span data-stu-id="b821e-110">If the request is approved, the server engine takes the request, and any properties requested by the Policy Module, and builds a complete certificate.</span></span>

4.  <span data-ttu-id="b821e-111">憑證發佈。</span><span class="sxs-lookup"><span data-stu-id="b821e-111">Certificate publication.</span></span>

    <span data-ttu-id="b821e-112">伺服器引擎會將已完成的憑證儲存在憑證服務資料庫中，並通知中繼應用程式要求狀態。</span><span class="sxs-lookup"><span data-stu-id="b821e-112">The server engine stores the completed certificate in the Certificate Services database and notifies the intermediary application of the request status.</span></span> <span data-ttu-id="b821e-113">如果結束 [模組](exit-modules.md) 有這樣的要求，伺服器引擎會通知它有憑證發佈事件。</span><span class="sxs-lookup"><span data-stu-id="b821e-113">If the [exit module](exit-modules.md) has so requested, the server engine will notify it of a certificate issuance event.</span></span> <span data-ttu-id="b821e-114">這可讓結束模組執行進一步的作業，例如將憑證發佈至外部憑證儲存機制 (例如目錄服務) 。</span><span class="sxs-lookup"><span data-stu-id="b821e-114">This allows the exit module to perform further operations such as publishing the certificate to an external certificate repository (for example, a directory service).</span></span> <span data-ttu-id="b821e-115">同時，中繼會從憑證服務取得已發佈的憑證，並將其傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="b821e-115">Meanwhile, the intermediary gets the published certificate from Certificate Services and passes it back to the client.</span></span>

<span data-ttu-id="b821e-116">下圖顯示憑證 [*要求*](../secgloss/c-gly.md) 如何由憑證服務處理。</span><span class="sxs-lookup"><span data-stu-id="b821e-116">The following illustration shows how a [*certificate request*](../secgloss/c-gly.md) is processed by Certificate Services.</span></span>

![處理憑證要求](images/certflow.png)

 

 
