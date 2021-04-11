---
title: 介面金鑰
description: 藉由將介面名稱與介面識別碼 (IID) 產生關聯，以註冊新的介面。 每個新介面都必須有一個 IID 子機碼。
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- 介面登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021807"
---
# <a name="interface-key"></a>介面金鑰

藉由將介面名稱與介面識別碼 (IID) 產生關聯，以註冊新的介面。 每個新介面都必須有一個 IID 子機碼。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ 介面** \\ *{* IID *}*



| 登錄值                               | Description                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Typeinterface**](baseinterface.md)       | 識別目前的介面衍生來源的介面。                                  |
| [**NumMethods**](nummethods.md)             | 包含相關聯介面中的方法數目，包括衍生介面的方法。 |
| [**ProxyStubClsid**](proxystubclsid.md)     | 將 IID 對應至16位 proxy Dll 中的 CLSID。                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | 將 IID 對應至32位 proxy Dll 中的 CLSID。                                                           |



 

## <a name="remarks"></a>備註

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**介面**](interface.md)
</dt> </dl>

 

 




