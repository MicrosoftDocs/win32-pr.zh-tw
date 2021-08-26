---
title: 隱含與明確的控制碼
description: 若要宣告序列化控制碼，請使用基本控制碼類型 handle \_ t。
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9f6dabc8a6e4d0e5ccac7ac8b94e1812d81a674b471015c868b32209fd9746
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020458"
---
# <a name="implicit-vs-explicit-handles"></a>隱含與明確的控制碼

若要宣告序列化控制碼，請使用基本控制碼類型 [**handle \_ t**](/windows/desktop/Midl/handle-t)。 序列化控制碼可以是明確或隱含的。 使用 **\[ 隱含 \_ 控制碼 \]** 屬性，在應用程式的 ACF 中指定隱含控制碼。 MIDL 編譯器將會產生全域序列化控制碼變數。 具有隱含控制碼的序列化程式會使用這個全域變數來存取有效的序列化內容。

使用類型編碼時，產生的常式支援特定型別的序列化，會使用全域隱含控制碼來存取序列化內容。 請注意，遠端常式可能需要使用隱含控制碼作為系結控制碼。 在進行序列化呼叫之前，請確定隱含控制碼已設定為有效的序列化控制碼。

明確的控制碼會指定為 IDL 檔案中序列化程式原型的參數，或者也可以使用 ACF 中的 **\[ 明確 \_ 控制碼 \]** 屬性來指定。 明確控制碼參數是用來建立程式的適當序列化內容。 為了在序列化類型的情況下建立正確的內容，編譯器會產生使用明確 [**控制碼 \_ t**](/windows/desktop/Midl/handle-t) 參數作為序列化控制碼的支援常式。 呼叫序列化程式或序列化型別支援常式時，必須提供有效的序列化控制碼。

 

 