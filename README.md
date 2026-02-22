import { PinataSDK } from "pinata";

const pinata = new PinataSDK({
  pinataJwt: process.env.PINATA_JWT!,
  pinataGateway: "example-gateway.mypinata.cloud",
});

const upload = await pinata.upload.public.json({
    content: "console.log('hello world!)",
    name: "helloworld.ts",
    lang: "ts"
})
type UploadResponse = {
	id: string;
	name: string;
	cid: string;
	size: number;
	created_at: string;
	number_of_files: number;
	mime_type: string;
	group_id: string | null;
	keyvalues: {
		[key: string]: string;
	};
	vectorized: boolean;
	network: string;
};const upload = await pinata.upload.public.json({
    content: "console.log('hello world!)",
    name: "helloworld.ts",
    lang: "ts"
})const upload = await pinata.upload.public
  .json({
    content: "console.log('hello world!)",
    name: "helloworld.ts",
    lang: "ts"
  })
  .group("b07da1ff-efa4-49af-bdea-9d95d8881103")const upload = await pinata.upload.public
  .json({
    content: "console.log('hello world!)",
    name: "helloworld.ts",
    lang: "ts"
  })
  .keyvalues({
    env: "prod"
  })const upload = await pinata.upload.public
  .json({
    content: "console.log('hello world!)",
    name: "helloworld.ts",
    lang: "ts"
  })
  .name("metadata.json")