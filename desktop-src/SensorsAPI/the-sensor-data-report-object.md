---
description: 感應器資料包表物件包含感應器資料。
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: 感應器資料包表物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944615"
---
# <a name="the-sensor-data-report-object"></a><span data-ttu-id="f126d-103">感應器資料包表物件</span><span class="sxs-lookup"><span data-stu-id="f126d-103">The Sensor Data Report Object</span></span>

<span data-ttu-id="f126d-104">感應器資料包表物件包含感應器資料。</span><span class="sxs-lookup"><span data-stu-id="f126d-104">The sensor data report object contains sensor data.</span></span>

<span data-ttu-id="f126d-105">感應器必須提供有意義的資料，才能發揮效用。</span><span class="sxs-lookup"><span data-stu-id="f126d-105">For a sensor to be useful, it must provide meaningful data.</span></span> <span data-ttu-id="f126d-106">資料產生的數量和頻率會因感應器而異。</span><span class="sxs-lookup"><span data-stu-id="f126d-106">The amount and frequency of data generation varies from sensor to sensor.</span></span> <span data-ttu-id="f126d-107">例如，偵測門是否開啟的感應器會產生少量的 **布林** 資料，而移動感應器可能會持續產生多個資料項目。</span><span class="sxs-lookup"><span data-stu-id="f126d-107">For example, a sensor that detects whether a door is open would generate a small amount of **Boolean** data, while a motion sensor might continuously generate multiple data items.</span></span> <span data-ttu-id="f126d-108">為了將您的程式接收資料的方式標準化，感應器 API 會使用感應器資料包表物件。</span><span class="sxs-lookup"><span data-stu-id="f126d-108">To standardize the way your program receives data, the Sensor API uses the sensor data report object.</span></span>

<span data-ttu-id="f126d-109">您可以透過 [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) 介面存取感應器資料包表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="f126d-109">You can access the information in a sensor data report through the [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) interface.</span></span> <span data-ttu-id="f126d-110">此介面可讓您抓取資料包表的時間戳記，以判斷報表中的資訊是否有用。</span><span class="sxs-lookup"><span data-stu-id="f126d-110">This interface lets you retrieve the data report's time stamp so that you can determine whether the information in the report is useful.</span></span> <span data-ttu-id="f126d-111">您可以使用兩種方式來抓取資料本身：作為個別資料欄值或一組值。</span><span class="sxs-lookup"><span data-stu-id="f126d-111">You can retrieve the data itself in two ways: as an individual data field value or as a set of values.</span></span> <span data-ttu-id="f126d-112">若要以個別值形式取出資料，請呼叫 [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) 方法。</span><span class="sxs-lookup"><span data-stu-id="f126d-112">To retrieve data as an individual value, call the [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) method.</span></span> <span data-ttu-id="f126d-113">若要取出多個值，請呼叫 [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) 方法。</span><span class="sxs-lookup"><span data-stu-id="f126d-113">To retrieve multiple values, call the [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) method.</span></span>

<span data-ttu-id="f126d-114">您可以使用 **PROPERTYKEY** 常數，指定要從報表中取出的資料類型或資料欄位。</span><span class="sxs-lookup"><span data-stu-id="f126d-114">You specify the type of data, or data fields, that you want to retrieve from the report by using a **PROPERTYKEY** constant.</span></span> <span data-ttu-id="f126d-115">一般感應器類型之資料欄位的屬性索引鍵是在 [感應器] 中定義。</span><span class="sxs-lookup"><span data-stu-id="f126d-115">Property keys for data fields of common sensor types are defined in Sensors.h.</span></span>

 

 
