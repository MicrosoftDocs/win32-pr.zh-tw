---
description: API 包含一種機制，可讓服務提供者廠商使用裝置特定的擴充功能來擴充電話語音 API。
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: 擴充的電話語音服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a319f59f51643fb5bf13ec95800d40ffa6d8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989947"
---
# <a name="extended-telephony-services"></a>擴充的電話語音服務

API 包含一種機制，可讓服務提供者廠商使用裝置特定的擴充功能來擴充電話語音 API。 擴充的電話語音服務 (或裝置特定的服務) 包含特定服務提供者所定義之 API 的所有延伸模組。 因為 API 只會定義擴充機制，所以服務提供者必須完全指定 Extended-Telephony 服務行為的定義。

## <a name="tapi-2x-extended-telephony"></a>TAPI 2.x 擴充電話語音

擴充機制可讓服務提供者廠商為某些列舉型別和位旗標定義新的值，並將成員新增至大部分的資料結構。 擴充功能的解讀會以服務提供者的延伸模組識別碼為依據，這是一組支援的延伸模組規格的識別碼，可跨數個製造商。 API 中會提供特殊的函式和訊息（例如 [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) 和 [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) ），以允許應用程式直接與服務提供者通訊。 服務提供者也會定義每個函數的參數。

廠商不需要註冊即可指派延伸模組識別碼。 相反地，會在平臺軟體發展工具組中提供稱為 EXTIDGEN (Extidgen.exe) 的公用程式， (SDK) 允許本機產生延伸模組識別碼。 這個唯一的識別碼是由乙太網路介面卡位址、亂數字和一天中的時間所組成。 在散發) 之前，會將識別碼指派給一組延伸 (，而不是指派給這些擴充功能的每個個別實例。

 

 
