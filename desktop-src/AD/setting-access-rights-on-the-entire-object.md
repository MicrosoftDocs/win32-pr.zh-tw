---
title: 設定整個物件的存取權限
description: 您只能針對整個物件（例如刪除和列出內容）設定某些許可權。 您也可以針對整個物件設定作業特定許可權（例如讀取權限），以便將它們套用至整個物件。
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- 設定整個物件 AD 的存取權限
- 物件 AD，設定存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462817"
---
# <a name="setting-access-rights-on-the-entire-object"></a>設定整個物件的存取權限

您只能針對整個物件（例如刪除和列出內容）設定某些許可權。 您也可以針對整個物件設定作業特定許可權（例如讀取權限），以便將它們套用至整個物件。

您可以使用下列程式來設定整個物件的許可權。

**若要設定整個物件的許可權**

1.  將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ AceType \_ 存取 \_ 允許** 或 **ads \_ AceType \_ \_ 拒絕存取**。
2.  將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 與 **IADsAccessControlEntry. InheritedObjectType** 設定為 **Null**。

如需有關如何建立 ACE 的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

如需可用於設定 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

 

 