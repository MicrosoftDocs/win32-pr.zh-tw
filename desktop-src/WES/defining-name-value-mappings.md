---
title: 定義名稱/值對應
description: 提供者可以定義客戶用來將整數值對應至字串的成對名稱/值組清單。
ms.assetid: d16b2410-a0de-42da-8f2a-98341c90ed87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62020adeb46bac96cada70cf5830e17213d69868
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104374869"
---
# <a name="defining-namevalue-mappings"></a><span data-ttu-id="b63e7-103">定義名稱/值對應</span><span class="sxs-lookup"><span data-stu-id="b63e7-103">Defining Name/Value Mappings</span></span>

<span data-ttu-id="b63e7-104">提供者可以定義客戶用來將整數值對應至字串的成對名稱/值組清單。</span><span class="sxs-lookup"><span data-stu-id="b63e7-104">A provider can define a list of name/value pairs that consumers use to map integer values to strings.</span></span> <span data-ttu-id="b63e7-105">名稱/值組可將整數值對應至字串，並將位值的位值對應至字串;每個值都會對應至字串值。</span><span class="sxs-lookup"><span data-stu-id="b63e7-105">The name/value pairs can map integer values to strings or bit values bit values to strings; each value corresponds to a string value.</span></span> <span data-ttu-id="b63e7-106">在包含列舉值的整數資料項目上使用對應。</span><span class="sxs-lookup"><span data-stu-id="b63e7-106">Use mappings on integer data items that contain enumeration values.</span></span>

<span data-ttu-id="b63e7-107">取用者可以使用值對應來取出與值相關聯的字串，並顯示該值，而不是顯示整數或位值。</span><span class="sxs-lookup"><span data-stu-id="b63e7-107">Consumers can use the value map to retrieve the string associated with a value and display it instead of displaying the integer or bit value.</span></span> <span data-ttu-id="b63e7-108">若要定義整數值對應，請使用 **valueMap** 和 **map** 元素。</span><span class="sxs-lookup"><span data-stu-id="b63e7-108">To define an integer value map, use the **valueMap** and **map** elements.</span></span> <span data-ttu-id="b63e7-109">若要定義位值對應，請使用 **bitmap** 和 **map** 元素。</span><span class="sxs-lookup"><span data-stu-id="b63e7-109">To define a bit value map, use the **bitmap** and **map** elements.</span></span>

<span data-ttu-id="b63e7-110">下列範例顯示如何定義值對應和點陣圖。</span><span class="sxs-lookup"><span data-stu-id="b63e7-110">The following example shows how to define a value map and a bitmap.</span></span> <span data-ttu-id="b63e7-111">您必須指定對應的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b63e7-111">You must specify the map's **name** attribute.</span></span> <span data-ttu-id="b63e7-112">針對每個名稱/值組，您必須指定 **value** 和 **message** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b63e7-112">For each name/value pair, you must specify the **value** and **message** attribute.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
