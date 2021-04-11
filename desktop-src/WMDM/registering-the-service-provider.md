---
title: 註冊服務提供者
description: 註冊服務提供者
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media 裝置管理員，註冊服務提供者
- 裝置管理員，註冊服務提供者
- 程式設計指南，註冊服務提供者
- 服務提供者，註冊服務提供者
- 建立服務提供者，註冊服務提供者
- 註冊服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020986"
---
# <a name="registering-the-service-provider"></a>註冊服務提供者

除了註冊為 COM 物件之外，服務提供者還必須註冊為 Windows Media 裝置管理員的外掛程式。 若要註冊，服務提供者必須建立下列登錄機碼：

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

在此機碼中，< *您的服務提供者名稱* > 是您的 DLL 名稱;例如，範例服務提供者會使用 MsHDSP。 ProgID 索引鍵應具有對應至服務提供者 CLSID 的字串值。 例如，範例服務提供者的值為 "MDServiceProviderHD. MDServiceProviderHD"。

當您註冊範例服務提供者 DLL 時，服務提供者在 Mdsp 中的 DLLRegisterServer 執行範例會新增此登錄機碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> </dl>

 

 




