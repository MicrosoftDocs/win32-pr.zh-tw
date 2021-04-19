---
description: 建立命名空間的另一個方法是使用 WMI API，以程式設計方式建立命名空間。
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: 使用 WMI API 建立命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977847"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>使用 WMI API 建立命名空間

建立命名空間的另一個方法是使用 WMI API，以程式設計方式建立命名空間。 以程式設計方式建立命名空間的優點是您可以從應用程式內建立命名空間。 不過，使用 WMI API 比使用受控物件格式 (MOF) 程式碼更複雜，而且您無法輕鬆地與其他開發人員共用您的命名空間。

下列程式描述如何使用 WMI API 建立命名空間。

**使用 WMI API 建立命名空間**

1.  使用 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)來抓取指向 [**\_ \_ 命名空間**](--namespace.md)系統類別之 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)物件的指標。
2.  使用 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)的呼叫來定義 [**\_ \_ 命名空間**](--namespace.md)系統類別的實例。
3.  使用 IWbemClassObject 的呼叫來設定 [**\_ \_ 命名空間**](--namespace.md)實例的 **Name** 屬性 [**：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)]。
4.  使用對 [**IWbemServices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)的呼叫來建立命名空間。

    [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)的 *pInst* 參數應指向新的實例。

 

 



