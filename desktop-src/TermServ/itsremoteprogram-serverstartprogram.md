---
title: ITSRemoteProgram ServerStartProgram 方法
description: 指定要在遠端會話中啟動的 RemoteApp 程式。
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- ServerStartProgram 方法遠端桌面服務
- ServerStartProgram 方法遠端桌面服務，ITSRemoteProgram 介面
- ITSRemoteProgram 介面遠端桌面服務，ServerStartProgram 方法
- ServerStartProgram 方法遠端桌面服務，ITSRemoteProgram2 介面
- ITSRemoteProgram2 介面遠端桌面服務，ServerStartProgram 方法
- ServerStartProgram 方法遠端桌面服務，ITSRemoteProgram3 介面
- ITSRemoteProgram3 介面遠端桌面服務，ServerStartProgram 方法
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508752"
---
# <a name="itsremoteprogramserverstartprogram-method"></a><span data-ttu-id="a1d43-110">ITSRemoteProgram：： ServerStartProgram 方法</span><span class="sxs-lookup"><span data-stu-id="a1d43-110">ITSRemoteProgram::ServerStartProgram method</span></span>

<span data-ttu-id="a1d43-111">指定要在遠端會話中啟動的 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="a1d43-111">Specifies a RemoteApp program to start in the remote session.</span></span> <span data-ttu-id="a1d43-112">當用戶端) 收到會話連線通知之後，就必須在連線的會話上叫用此函數 (。</span><span class="sxs-lookup"><span data-stu-id="a1d43-112">This function must be invoked on a connected session (after the session connected notification is received at the client).</span></span> <span data-ttu-id="a1d43-113">任何數目的 RemoteApp 程式都可以在會話中啟動。</span><span class="sxs-lookup"><span data-stu-id="a1d43-113">Any number of RemoteApp programs can be started in a session.</span></span> <span data-ttu-id="a1d43-114">如果沒有在會話中啟動 RemoteApp 程式（Windows Server 2008 的兩分鐘），RemoteApp 會話將會超時。</span><span class="sxs-lookup"><span data-stu-id="a1d43-114">A RemoteApp session will time out if no RemoteApp program is started in the session within the time-out limit, which is two minutes for Windows Server 2008.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d43-115">語法</span><span class="sxs-lookup"><span data-stu-id="a1d43-115">Syntax</span></span>


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="a1d43-116">參數</span><span class="sxs-lookup"><span data-stu-id="a1d43-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d43-117">*bstrExecutablePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1d43-117">*bstrExecutablePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d43-118">伺服器上 RemoteApp 程式可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="a1d43-118">The path of the RemoteApp program executable file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="a1d43-119">*bstrFilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1d43-119">*bstrFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d43-120">要在伺服器上透過檔案關聯開啟的檔案路徑，例如 "C： \\ \\ Documents \\ \\MyReport.docx"。</span><span class="sxs-lookup"><span data-stu-id="a1d43-120">The path of a file to open on the server through a file association, for example "C:\\\\Documents\\\\MyReport.docx".</span></span> <span data-ttu-id="a1d43-121">如果您指定 *bstrFilePath*，則不應指定 *bstrExecutablePath* 參數，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="a1d43-121">If you specify *bstrFilePath*, you should not specify the *bstrExecutablePath* parameter, and vice versa.</span></span> <span data-ttu-id="a1d43-122">您應該只指定其中一個參數。</span><span class="sxs-lookup"><span data-stu-id="a1d43-122">You should only specify one of the parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a1d43-123">*bstrWorkingDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1d43-123">*bstrWorkingDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d43-124">適用于 RemoteApp 程式之伺服器上的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="a1d43-124">The working directory on the server for the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="a1d43-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1d43-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d43-126">指出伺服器是否應在工作目錄路徑中展開環境變數。</span><span class="sxs-lookup"><span data-stu-id="a1d43-126">Indicates whether the server should expand environment variables in the working directory path.</span></span> <span data-ttu-id="a1d43-127">如果工作目錄路徑包含環境變數，則將此參數設定為 **variant \_ TRUE** ，如果工作目錄路徑不包含環境變數，則為 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a1d43-127">Set this parameter to **VARIANT\_TRUE** if the working directory path contains environment variables, or **VARIANT\_FALSE** if the working directory path does not contain environment variables.</span></span>

</dd> <dt>

<span data-ttu-id="a1d43-128">*bstrArguments* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1d43-128">*bstrArguments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d43-129">在 *bstrExecutablePath* 中指定之 RemoteApp 程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="a1d43-129">The command-line arguments for the RemoteApp program that are specified in *bstrExecutablePath*.</span></span> <span data-ttu-id="a1d43-130">如果未指定 *bstrExecutablePath* ，請將此值設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a1d43-130">Set this to **NULL** if *bstrExecutablePath* is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="a1d43-131">*vbExpandEnvVarInArgumentsOnServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1d43-131">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d43-132">指出伺服器是否應展開命令列引數中的環境變數。</span><span class="sxs-lookup"><span data-stu-id="a1d43-132">Indicates whether the server should expand environment variables in the command-line arguments.</span></span> <span data-ttu-id="a1d43-133">如果引數包含環境變數，則將此參數設定為 **variant \_ TRUE** ，如果引數不包含環境變數，則為 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a1d43-133">Set this parameter to **VARIANT\_TRUE** if the arguments contain environment variables, or **VARIANT\_FALSE** if the arguments do not contain environment variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1d43-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1d43-134">Return value</span></span>

<span data-ttu-id="a1d43-135">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="a1d43-135">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d43-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1d43-136">Requirements</span></span>



| <span data-ttu-id="a1d43-137">需求</span><span class="sxs-lookup"><span data-stu-id="a1d43-137">Requirement</span></span> | <span data-ttu-id="a1d43-138">值</span><span class="sxs-lookup"><span data-stu-id="a1d43-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d43-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1d43-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d43-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1d43-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a1d43-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1d43-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d43-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1d43-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a1d43-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a1d43-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1d43-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1d43-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1d43-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a1d43-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1d43-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1d43-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1d43-147">IID</span><span class="sxs-lookup"><span data-stu-id="a1d43-147">IID</span></span><br/>                      | <span data-ttu-id="a1d43-148">IID \_ ITSRemoteProgram 定義為 FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="a1d43-148">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a1d43-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1d43-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d43-150">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="a1d43-150">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="a1d43-151">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="a1d43-151">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="a1d43-152">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="a1d43-152">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





