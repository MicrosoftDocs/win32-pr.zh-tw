---
description: Windows通訊端2提供一組展開的作業，可以一致地建立通訊端連接。 下列說明執行這些功能的服務提供者需求。
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: 連線時間的增強功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70be979fc807a2de25d44eb90e9d344124963d12d42863447d335b4b7e4937f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132651"
---
# <a name="enhanced-functionality-at-connect-time"></a>連線時間的增強功能

Windows通訊端2提供一組展開的作業，可以一致地建立通訊端連接。 下列說明執行這些功能的服務提供者需求。

## <a name="conditional-acceptance"></a>條件式接受

如先前所述， [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) 會叫用用戶端提供的條件函式，該函式會使用輸入參數來提供擱置連接要求的相關資訊。 用戶端可以使用此資訊，根據呼叫端資訊（例如呼叫端識別碼、QoS 等）來接受或拒絕連接要求。如果條件函式傳回 CF \_ ACCEPT，則會使用與接聽通訊端相同的屬性來建立新的通訊端，並傳回新通訊端的控制碼。 如果條件函數傳回 CF \_ 拒絕，則應該拒絕連線要求。 如果條件函式傳回 CF \_ 延遲，即無法立即進行接受/拒絕決策，且服務提供者必須在待處理專案佇列中保留連接要求。 用戶端必須重新呼叫 **WSPAccept** （當它準備好進行決策時），並排列條件函式以傳回 cf \_ ACCEPT 或 cf \_ 拒絕。 當延遲的連接要求位於待處理專案佇列的最上方時，服務提供者不會針對擱置的連接要求發出任何進一步的指示。

## <a name="exchanging-user-data-at-connect-time"></a>在連線時間交換使用者資料

某些通訊協定允許在連接時交換少量的使用者資料。 如果已從連線的主機接收這類資料，則會將它放在服務提供者緩衝區中，而這個緩衝區的指標和長度值會透過輸入參數提供給 Winsock SPI 用戶端，以供 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) 條件函數使用。 如果 Winsock SPI 用戶端具有回應資料以傳回連線的主機，它可能會將它複製到服務提供者所提供的緩衝區。 此緩衝區的指標和表示緩衝區大小的整數，也會以條件函數輸入參數的形式提供， (如果通訊協定) 支援的話。

## <a name="establishing-socket-groups"></a>建立通訊端群組

通訊端群組的所有使用都是保留的。

 

 



