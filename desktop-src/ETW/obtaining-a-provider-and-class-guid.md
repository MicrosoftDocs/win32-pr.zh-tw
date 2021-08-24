---
description: 若要取得提供者 GUID 或事件追蹤類別 Guid，您可以使用 Uuidgen.exe 或 Guidgen.exe 工具。
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: 取得提供者和類別 GUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c480a45a5a826d3f258ab267e39db87bc85fad799fef5d7397a7c900f4872f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914348"
---
# <a name="obtaining-a-provider-and-class-guid"></a>取得提供者和類別 GUID

若要取得提供者 GUID 或事件追蹤類別 Guid，您可以使用 Uuidgen.exe 或 Guidgen.exe 工具。

如果您使用 Uuidgen.exe 工具，請使用-d 選項來建立定義 \_ GUID C 宏，如下列範例所示。 如需使用 Uuidgen.exe 工具的相關資訊，請使用-？ 選項。 如果您使用「定義 \_ Guid C」宏來定義您的 guid，您必須在 \# guid 定義之前包含「定義 INITGUID」，如下列範例所示。

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

Microsoft Windows 軟體開發套件 (SDK) 和 Microsoft Visual Studio 包含 Guidgen.exe 工具。 Guidgen.exe 工具有一個使用者介面，可讓您從數種格式中進行選取。 您應使用可建立靜態常數 GUID 的格式，如下列範例所示。

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



