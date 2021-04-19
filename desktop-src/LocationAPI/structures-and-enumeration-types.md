---
description: 位置 API 會定義下列列舉類型。
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: " (位置 API) 的結構和列舉類型"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978040"
---
# <a name="structures-and-enumeration-types-location-api"></a> (位置 API) 的結構和列舉類型

\[Win32 位置 API 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。 \]

位置 API 會定義下列列舉類型。



| 列舉型別                                                                       | 描述                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**需要的位置 \_ \_ 精確度**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))                  | 定義可能需要的精確度類型。                         |
| [**位置 \_ 報告 \_ 狀態**](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | 針對特定報表類型的新報表定義可能的狀態。 |



 

## <a name="location-constants-from-the-sensor-api"></a>來自感應器 API 的位置常數

感應器 API 也會定義位置相關的屬性索引鍵和常數。 您可以藉由呼叫 [**ILocationReport：： GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue)，使用在 [感應器] 中定義的屬性索引鍵來從報表取出位置資料。

 

 
