---
description: 提供安全性內容的安全通道特定資訊。
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: 查詢 Schannel 內容的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f00f6d5f0660bbb3a0d4ce5890ab415325707dbda4087d025a010efdb3fd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919937"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>查詢 Schannel 內容的屬性

[**QueryCoNtextAttributes (schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw)函數提供 [*安全性內容的安全*](../secgloss/s-gly.md)通道特定資訊。 大部分的資訊最初是在使用用戶端 [**InitializeSecurityCoNtext (schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) 或伺服器 [**AcceptSecurityCoNtext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式建立內容時所指定。 取得用來建立內容之認證的控制碼時，會指定一些資訊。 如需詳細資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。

 

 
