---
title: 安裝 EAP 方法
description: 請遵循下列指示，在執行 EAPHost 的用戶端電腦上安裝使用者所執行的 EAP 方法。
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682104"
---
# <a name="installing-an-eap-method"></a>安裝 EAP 方法

請遵循下列指示，在執行 EAPHost 的用戶端電腦上安裝使用者所執行的 EAP 方法。

-   為您的 EAP 方法 DLL 執行 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 。 這些函式會在安裝期間為您的 EAP 方法新增和移除適當的登錄機碼，並 (卸載) 進程。

    如需與 EAP 方法安裝相關聯之特定登錄機碼的詳細資訊，請參閱 [Eap 方法](registry-keys-for-eap-methods.md) 的登錄設定主題。

-   使用下列主控台命令安裝含有 EAP 方法的 DLL。

    **regsvr32.exe** *&lt; DLL 名稱 &gt;*

    若要卸載 DLL，請使用下列主控台命令：

    **regsvr32.exe** **/u** *&lt; DLL 名稱 &gt;*

-   重新開機 EAPHost 服務。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 EAPHost](using-eap-host.md)
</dt> </dl>

 

 