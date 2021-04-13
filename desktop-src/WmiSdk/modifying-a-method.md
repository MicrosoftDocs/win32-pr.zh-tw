---
description: 除了類別和實例之外，WMI 還可讓您修改方法。 您會想要修改方法的主要原因是您變更了提供者中方法的執行方式。 如需詳細資訊，請參閱撰寫方法提供者。
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: 修改方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386059"
---
# <a name="modifying-a-method"></a>修改方法

除了類別和實例之外，WMI 還可讓您修改方法。 您會想要修改方法的主要原因是您變更了提供者中方法的執行方式。 如需詳細資訊，請參閱 [撰寫方法提供者](writing-a-method-provider.md)。

修改方法不是可以在腳本中完成的作業。

下列程式描述如何以程式設計方式修改方法。

**以程式設計方式修改方法**

1.  使用 [**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)的呼叫來取出類別定義。

    *PpInSignature* 和 *ppOutSignature* 這兩個 out 參數分別包含 in 參數類別和 out 參數類別。 傳回值會以屬性的形式組合在 out 參數類別中，而且應該命名為 **ReturnValue**。

2.  使用對 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)、 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)內容或 [**IWbemClassObject：:D elete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)的呼叫來抓取和修改參數。
3.  呼叫 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)，將新版本的方法放回父類別。

如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

 

 



