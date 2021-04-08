---
title: 基本 RPC 系結術語
description: 為了進一步協助用戶端/伺服器連接程式的討論，瞭解下列詞彙會很有説明。
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- 遠端程序呼叫 RPC、描述、系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023926"
---
# <a name="essential-rpc-binding-terminology"></a>基本 RPC 系結術語

為了進一步協助用戶端/伺服器連接程式的討論，瞭解下列詞彙會很有説明。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>通訊協定順序
</dt> <dd>

當網路作業系統彼此通訊時，他們必須接聽並說出相同的語言。 這些語言稱為 *通訊協定順序*。 用戶端和伺服器程式必須使用連接它們所支援之網路的通訊協定順序。 Microsoft RPC 支援各種不同的通訊協定順序。 如需詳細資訊，請參閱 [選取通訊協定順序](selecting-a-protocol-sequence.md)， [指定通訊協定](specifying-protocol-sequences.md)順序和 [**端點**](/windows/desktop/Midl/endpoint)。

</dd> <dt>

<span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>伺服器主機電腦或伺服器主機系統
</dt> <dd>

伺服器程式會在伺服器主機電腦上執行。 不過，用戶端/伺服器運算的許多文獻都指的是伺服器程式和伺服器主機電腦做為「伺服器」。 結果就是，它不一定是很清楚的討論。

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點
</dt> <dd>

伺服器程式會接聽伺服器主機電腦上的埠或通訊埠群組，以取得用戶端要求。 伺服器主機系統會維護這些埠的資料庫，這些埠稱為 RPC 中的端點。 資料庫稱為端點對應。

</dd> <dt>

<span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>綁定
</dt> <dd>

用戶端程式會建立伺服器的系結，以建立通訊會話。 系結包含用戶端應用程式建立會話所需的所有資訊。

</dd> </dl>

 

 