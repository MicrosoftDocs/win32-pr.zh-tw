---
title: 程式序列化
description: 當您使用程式序列化時，會使用 \ 編碼 \ 或 \ 解碼 \ 屬性來標記程式。 編譯器不會產生一般的遠端存根，而是會產生常式的序列化存根。
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b514aa5a2e5be1b937a3989c3446bcc6e61c76f885381ce257286b5c625b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018948"
---
# <a name="procedure-serialization"></a>程式序列化

當您使用程式序列化時，會使用 \[ [**編碼**](/windows/desktop/Midl/encode) \] 或解碼 \[ [](/windows/desktop/Midl/decode) \] 屬性來標記程式。 編譯器不會產生一般的遠端存根，而是會產生常式的序列化存根。

就像遠端程式必須使用系結控制碼進行遠端呼叫，序列化程式必須使用序列化控制碼來使用序列化服務。 如果未指定序列化控制碼，則會使用預設的隱含控制碼來指示呼叫。 另一方面，如果指定了序列化控制碼（以做為常式的明確 [**控制碼 \_ t**](/windows/desktop/Midl/handle-t)引數，或使用 \[ [**明確 \_ 控制碼**](/windows/desktop/Midl/explicit-handle) \] 屬性），則您必須傳遞有效的控制碼做為呼叫的引數。 如需有關如何建立有效序列化控制碼的詳細資訊，請參閱 [序列化控制碼](serialization-handles.md)、 [固定緩衝區編碼範例](fixed-buffer-serialization.md)和累加 [式編碼範例](examples-of-incremental-encoding.md)。

> [!Note]
> Microsoft RPC 允許將遠端和序列化程式混合在一個介面中。 但是，當您這麼做時，請特別小心。
> 
> 針對具有隱含系結控制碼的遠端程式，MIDL 編譯器會產生型 [**別控制碼 \_ t**](/windows/desktop/Midl/handle-t)的全域控制碼變數。 具有隱含序列化控制碼的程式和類型會使用這個相同的全域控制碼變數。
> 
> 若為隱含控制碼，全域隱含控制碼必須設定為有效的系結控制碼，才能進行遠端呼叫。 在序列化呼叫之前，隱含控制碼必須設定為有效的序列化控制碼。 因此，程式不能同時為遠端和序列化。 它必須是一個或另一個。

 

 

 