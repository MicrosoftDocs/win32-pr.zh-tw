---
title: 安裝 EAP 方法
description: 請遵循下列指示，在執行 EAPHost 的用戶端電腦上安裝使用者所執行的 EAP 方法。
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e047c5a8f0bc4cedcc207016d6f66530b392869839dda128635cd31ac459011a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021578"
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

 

 