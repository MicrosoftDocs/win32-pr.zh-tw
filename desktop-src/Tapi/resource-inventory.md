---
description: 應用程式必須清查其可用的通訊資源，然後通知 TAPI 將使用的資源，以及其使用方式。
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: 資源清查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979140"
---
# <a name="resource-inventory"></a>資源清查

應用程式必須清查其可用的通訊資源，然後通知 TAPI 將使用的資源，以及其使用方式。 如需應用程式可能存取的資源和功能類型的其他資訊，請參閱 [裝置控制](device-control.md) 。

**TAPI 2.x：** 應用程式會在 [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) 傳回時取得可用的行數。 然後，他們可以在每一行執行 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) 、針對每個位址 [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) ，以及針對將使用的每一行 [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) 。

**TAPI 3.x：** 應用程式會使用 [**ITTAPI：： EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) 或 [**ITTAPI：： get \_ 位址**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) 來探索可用的位址。 [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) 和 [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) 提供每個位址可能的通訊類型資訊。 如果由服務提供者所執行， [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) 會讓應用程式存取其他資訊和控制項。

 

 
